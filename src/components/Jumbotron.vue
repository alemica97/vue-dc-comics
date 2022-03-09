<template>
    <main class="main-wrapper">
        <div class="container">
          <button class="jumbo-button">{{buttonText}}</button>
        </div>
    </main>
</template>

<script>
export default {
  name: 'myJumbotron',
  data(){
    return{
        buttonText: 'current series',
    }
  }
}
</script>

<style scoped lang="scss">

  .main-wrapper{
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: 50% 0%;
    background-size: cover;
    background-repeat: no-repeat;
    height: 400px;
  }

  .container{
    position: relative;
  }

  .jumbo-button{
    background-color: #0282F9;
    border: none;
    padding: 10px 20px;
    color: white;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 700;
    position: absolute;
    top: 385px;
    left: 0;
  }

</style>