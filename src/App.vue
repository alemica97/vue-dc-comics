<template>
  <div id="app">
    <!-- header and nav bar  -->
    <myHeader />
    <!-- main -->
    <myJumbotron />
    <!-- footer -->
    <topFooter />
    <myFooter />
  </div>
</template>

<script>
import myHeader from './components/Header.vue'
import myJumbotron from './components/Jumbotron.vue'
import topFooter from './components/topFooter.vue'
import myFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myJumbotron,
    topFooter,
    myFooter,
  }
}
</script>

<style lang="scss">
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    ul, li{
        list-style-type: none;
    }

    a{
        text-decoration: none;
        color: currentColor;
    }

    img{
        max-width: 100%;
        max-height: 100%;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
    }

    .container{
        margin: 0 auto;
        max-width: 1300px;
    }

    .container-small{
      max-width: 450px;
    }
</style>
