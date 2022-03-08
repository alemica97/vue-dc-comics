<template>
    <footer>
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

        <div class="footer-link">
            <div class="container">
                <div class="container-small">

                    <ul v-for="(list, i) in footerList" :key="i">
                        <li class="list-title">
                            <h3>{{ list.title }}</h3>
                        </li>
                        <li v-for="(item, index) in list.listLink" :key="index" class="list-item">
                            {{ item.text }}
                        </li>
                    </ul>
                </div>
                <div class="logo-wrapper">
                    <!-- <figure>
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </figure> -->
                </div>
            </div>
        </div>

        <div class="footer-social"></div>
    </footer>
</template>

<script>
export default {
  name: 'myFooter',
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
          
          footerList: [
              {
                  title: 'dc comics',
                  listLink: [
                      {
                          text: 'Characters',
                      },
                      {
                          text: 'Comics',
                      },
                      {
                          text: 'Movies',
                      },
                      {
                          text: 'TV',
                      },
                      {
                          text: 'Games',
                      },
                      {
                          text: 'Videos',
                      },
                      {
                          text: 'News',
                      },
                  ],
              },
              {
                  title: 'dc',
                  listLink: [
                      {
                          text: 'Term Of Use',
                      },
                      {
                          text: 'Privacy polici (New)',
                      },
                      {
                          text: 'Ad Choices',
                      },
                      {
                          text: 'Advertising',
                      },
                      {
                          text: 'Jobs',
                      },
                      {
                          text: 'Subscription',
                      },
                      {
                          text: 'Talent Workshops',
                      },
                      {
                          text: 'CPSC Certificates',
                      },
                      {
                          text: 'Ratings',
                      },
                      {
                          text: 'Shop Help',
                      },
                      {
                          text: 'Contact Us',
                      },
                  ],
              },
              {
                  title: 'sites',
                  listLink: [
                      {
                          text: 'DC',
                      },
                      {
                          text: 'MAD Magazine',
                      },
                      {
                          text: 'DC Kids',
                      },
                      {
                          text: 'DC Universe',
                      },
                      {
                          text: 'DC Power Visa',
                      },
                  ],
              },
              {
                  title: 'shop',
                  listLink: [
                      {
                          text: 'Shop DC',
                      },
                      {
                          text: 'Shop DC Collectibles',
                      },
                  ],
              },
          ],
      }
  },
}
</script>

<style scoped lang="scss">

  .footer-header{
    background-color: #0282F9;
    padding: 50px 20px;

    & .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 10px;

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
        justify-content: space-around;
        align-items: center;
        gap: 10px;

        & a{
            text-transform: uppercase;
            color: white;
            font-size: 15px;
            font-weight: 500;

            &:hover{
                transform: scale(1.05, 1.05);
            }
        }
    }

    .list-title{
        font-size: 16px;
        margin-bottom: 15px;
        text-transform: uppercase;
        color: white;
    }

    .list-item{
        font-size: 14px;
        margin-bottom: 10px;
        color: white;
        opacity: 0.6;

        &:hover{
            opacity: 1;
            cursor: pointer;
        }
    }

    .container-small{
        padding: 40px 10px 60px 0px;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        flex-wrap: wrap;
        column-gap: 50px;

        & ul{
            display: inline-block;
        }
        
    }

    .footer-link{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

</style>