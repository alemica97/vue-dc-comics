<template>
  <div id="app">
    <!-- header and nav bar  -->
    <myHeader />
    <!-- main -->
    <myMain />
    <!-- footer -->
    <myFooter />
  </div>
</template>

<script>
import myHeader from './components/Header.vue'
import myMain from './components/Main.vue'
import myFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myMain,
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

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
