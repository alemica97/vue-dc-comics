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
            </div>
        </div>

        <div class="footer-social">
            <div class="container">
                <div>
                    <button class="sign-up">
                        <span>sign-up now!</span>
                    </button>
                </div>
                <div class="social-section">
                    <button class="follow">
                        <span>follow us</span>
                    </button>
                    <ul>
                        <li v-for="(icon, i) in socialIcons" :key="i" class="social-icon">
                            <a :href="icon.href">
                                <img :src="icon.image" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
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
          socialIcons: [
              {
                  image: require('../assets/img/footer-facebook.png'),
                  href: '#',
              },
              {
                  image: require('../assets/img/footer-twitter.png'),
                  href: '#',
              },
              {
                  image: require('../assets/img/footer-youtube.png'),
                  href: '#',
              },
              {
                  image: require('../assets/img/footer-pinterest.png'),
                  href: '#',
              },
              {
                  image: require('../assets/img/footer-periscope.png'),
                  href: '#',
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
            font-weight: 500;
            white-space: nowrap;

            &:hover{
                transform: scale(1.05, 1.05);
            }
        }
    }

    .list-title{
        font-size: 15px;
        margin-bottom: 15px;
        text-transform: uppercase;
        color: white;
    }

    .list-item{
        font-size: 12px;
        margin-bottom: 10px;
        color: white;
        opacity: 0.6;

        &:hover{
            opacity: 1;
            cursor: pointer;
        }
    }

    .container-small{
        padding: 40px 0px 60px 10px;
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
        background-image: url(../assets/img/dc-logo-bg.png) ,url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: calc(30px + 40vw) , cover;
        background-position: 80% center ,center;
    }

    .footer-social{
        height: 110px;
        background-color: #303030;
        color: white;

        & ul{
            display: contents;
        }

        & .container{
            display: flex;
            justify-content: flex-start;
            align-items: center;
            height: 100%;
            padding: 0 10px;
        }
    }

    .social-section{
        display: flex;
        justify-content: flex-end;
        align-items: center;
        flex-grow: 1;
        gap: 15px;
    }

    .sign-up{
        color: white;
        border: 2px solid #0282F9;
        padding: 15px;

        &:hover{
            cursor: pointer;
            background-color: rgba(255, 255, 255, 0.8);
            color: #0282F9;
            transition: all 500ms;
        }
    }

    .follow{
        color: #0282F9;
        border: none;
    }

    .sign-up, .follow{
        text-transform: uppercase;
        background-color: transparent;
        font-size: 18px;
        font-weight: 550;
    }

    .social-icon:hover{
        transform: scale(1.05, 1.05);
    }

</style>