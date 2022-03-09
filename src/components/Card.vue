<template>
    <div class="card-wrapper">
        <figure class="image-wrapper">
            <img :src="cardImg" alt="">
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
    }
}
</script>

<style lang="scss" scoped>

    .card-wrapper{
        width: 185px;
        text-align: center;
        display: flex;
        flex-direction: column;
        row-gap: 20px;
    }
    .image-wrapper{
        width: 100%;
        height: 185px;
    }

    .image-wrapper > img{
        object-fit: cover;
        object-position: center;
        overflow: hidden;
    }

    .card-par{
        color: white;
        text-transform: uppercase;
        font-size: 15px;
    }
</style>
