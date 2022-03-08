<template>
    <footer>
        <div class="footer-header">
          <div class="container">
            <ul>
              <li class="merch-link">
                <figure>
                  <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                </figure>
                <a href="">digital comics</a>
              </li>
              <li class="merch-link">
                <figure>
                    <img src="../assets/img/buy-comics-merchandise.png" alt="">
                </figure>
                <a href="">dc merchandise</a>
              </li>
              <li class="merch-link">
                <figure>
                    <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                </figure>
                <a href="">subscription</a>
              </li>
              <li class="merch-link">
                <figure>
                    <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                </figure>
                <a href="">comic shop locator</a>
              </li>
              <li class="merch-link">
                <figure>
                    <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                </figure>
                <a href="">dc power visa</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="footer-link"></div>
        <div class="footer-social"></div>
    </footer>
</template>

<script>
export default {
  name: 'myFooter',
}
</script>

<style scoped lang="scss">

  .footer-header{
    background-color: #0282F9;
    padding: 50px 10px;
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

    ul{
        display: contents;
    }

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 10px;
    }
</style>