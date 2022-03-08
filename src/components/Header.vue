<template>
    <header class="header">
        <div class="container">
            <figure class="main-logo">
                <img src="../assets/img/dc-logo.png">
            </figure>
            <nav class="navbar">
                <ul>
                    <li v-for="(element, i) in navbarArray" :key="i" class="navbar-items"
                        :class="activeNavElement == i ? 'active' : ''" @click="activeNavElement = i">
                        <a :href="element.href">{{ element.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: 'myHeader',
  data(){
      return{
          activeNavElement: null,

          navbarArray: [
              {
                  href: '',
                  text: 'characters'
              },
              {
                  href: '',
                  text: 'comics'
              },
              {
                  href: '',
                  text: 'movies'
              },
              {
                  href: '',
                  text: 'tv'
              },
              {
                  href: '',
                  text: 'games'
              },
              {
                  href: '',
                  text: 'collectibles'
              },
              {
                  href: '',
                  text: 'videos'
              },
              {
                  href: '',
                  text: 'fans'
              },
              {
                  href: '',
                  text: 'news'
              },
              {
                  href: '',
                  text: 'shop'
              }
          ],
      }
  }
}
</script>

<style scoped lang="scss">

    .header{
        height: 117px;
    }

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        padding: 0 10px;
    }

    .main-logo{
        width: 78px;
        height: 78px;
        flex-shrink: 0;
    }

    .navbar ul{
        display: contents;
    }

    .navbar{
        display: flex;
        justify-content: flex-end;
        align-items: center;
        column-gap: 30px;
        flex-grow: 1;
    }

    .navbar-items{
        text-transform: uppercase;
        font-weight: 700;
        font-size: 14px;
        color: #464646;
        height: 117px;
        line-height: 117px;

        &:hover, &.active{
            border-bottom: 5px solid #0282F9;
            a {
                color: #0282F9; 
            }
        }
    }

</style>