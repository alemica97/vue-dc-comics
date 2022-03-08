<template>
    <main class="main-wrapper">
        <div class="container">
          <h4>{{ mainTitle }}</h4>
        </div>
    </main>
</template>

<script>
export default {
  name: 'myMain',
  data(){
    return{
      mainTitle: '--> Content goes here <--'
    }
  }
}
</script>

<style scoped lang="scss">

  .main-wrapper{
    padding: 60px 10px;
    font-size: 20px;
    color: white;
    background-color: #464646;
  }

</style>