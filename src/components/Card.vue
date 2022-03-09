<template>
    <div class="card-wrapper">
        <figure class="image-wrapper">
            <img :src="cardImg" alt="">
            <span class="price">{{ cardPrice }}</span>
        </figure>
        <h3 class="card-par">{{ cardText }}</h3>
    </div>
</template>

<script>

export default {
    name: 'myCard',

    props: {
        cardImg: String,
        cardText: String,
        cardPrice: String,
    }
}
</script>

<style lang="scss" scoped>

    .card-wrapper{
        // width: calc((100% - 150px) / 6);
        width: 185px;
        text-align: center;
        display: flex;
        flex-direction: column;
        row-gap: 20px;
    }

    .image-wrapper{
        width: 100%;
        height: 185px;
        position: relative;

        &::after{
            content: '';
            display: none;
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-color: #0282f9ad;
        }

        &:hover::after{
            display: block;
            cursor: pointer;
        }

        &:hover img{
            object-position: 50% 30%;
            transition: all 500ms;
        }

        &:hover .price{
            display: block;
        }
    }

    .price{
        color: white;
        font-size: 50px;
        font-weight: 600;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50% , -50%);
        z-index: 999;
        display: none;
    }

    .image-wrapper > img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: 50% 0;
    }

    .card-par{
        color: white;
        text-transform: uppercase;
        font-size: 15px;
    }
</style>
