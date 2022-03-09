<template>
    <div class="footer-header">
          <div class="container">
            <ul>
              <li v-for="(element, i) in merchLinkArray" :key="i" class="merch-link">
                <figure>
                  <img :src="require('../assets/img/' + element.image)" alt="">
                </figure>
                <a :href="element.href">{{ element.text }}</a>
              </li>
            </ul>
          </div>
        </div>
</template>

<script>

export default{
    name: 'topFooter',
    data(){
        return{
            merchLinkArray: [
              {
                  image: 'buy-comics-digital-comics.png',
                  href: '#',
                  text: 'digital comics',
              },
              {
                  image: 'buy-comics-merchandise.png',
                  href: '#',
                  text: 'dc merchandise',
              },
              {
                  image: 'buy-comics-subscriptions.png',
                  href: '#',
                  text: 'subscription',
              },
              {
                  image: 'buy-comics-shop-locator.png',
                  href: '#',
                  text: 'comic shop locator',
              },
              {
                  image: 'buy-dc-power-visa.svg',
                  href: '#',
                  text: 'dc power visa',
              },
          ],
        }
    }
}

</script>

<style scoped lang="scss">

    .footer-header{
        background-color: #0282F9;
        padding: 50px 20px;

        & .container{
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;

            & > ul{
                display: contents;
            }
        } 
    }

    .merch-link figure{
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .merch-link{
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 5px;

        & a{
            text-transform: uppercase;
            color: white;
            font-size: 14px;
            font-weight: 700;
            white-space: nowrap;

            &:hover{
                transform: scale(1.05, 1.05);
            }
        }
    }
</style>