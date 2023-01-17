<script>
export default {
    name: 'SiteFooter',
    data() {
        return {
            brands: [
                {
                    image: 'footer-facebook.png'
                },
                {
                    image: 'footer-periscope.png'
                },
                {
                    image: 'footer-pinterest.png'
                },
                {
                    image: 'footer-twitter.png'
                },
                {
                    image: 'footer-youtube.png'
                },
            ],
            DcComics: [
                {
                    text: 'Characters'
                },
                {
                    text: 'Comics'
                },
                {
                    text: 'Movies'
                },
                {
                    text: 'TV'
                },
                {
                    text: 'Games'
                },
                {
                    text: 'Videos'
                },
                {
                    text: 'News'
                }
            ],
            Shop: [
                {
                    text: 'Shop DC'
                },
                {
                    text: 'Shop DC Collectibles'
                }
            ],
            DC: [
                {
                    text: 'Terms Of Use'
                },
                {
                    text: 'Privacy policy (New)'
                },
                {
                    text: 'Ad Choices'
                },
                {
                    text: 'Advertising'
                },
                {
                    text: 'Jobs'
                },
                {
                    text: 'Subscriptions'
                },
                {
                    text: 'Talent Workshops'
                },
                {
                    text: 'CPSC Certificates'
                },
                {
                    text: 'Ratings'
                },
                {
                    text: 'Shop Help'
                },
                {
                    text: 'Contact Us'
                },
            ],
            Sites: [
                {
                    text: 'DC'
                },
                {
                    text: 'MAD Magazine'
                },
                {
                    text: 'DC Kids'
                },
                {
                    text: 'DC Universe'
                },
                {
                    text: 'DC Power Visa'
                }
            ]
        }
    }
}
</script>

<template>
  <footer>
    <div class="background-section">
      <div class="container">
        <div class="link-section">
          <div class="link-col">
            <h3>dc comics</h3>
            <a href="#" v-for="item in DcComics">{{ item.text }}</a>
            <h3>shop</h3>
            <a href="#" v-for="item in Shop">{{ item.text }}</a>
          </div>
          <div class="link-col">
            <h3>DC</h3>
            <a href="#" v-for="item in DC">{{ item.text }}</a>
          </div>
          <div class="link-col">
              <h3>Sites</h3>
              <a href="#" v-for="item in Sites">{{ item.text }}</a>
          </div>
          <div class="background-img">
            <img class="logo-bg" src="/img/dc-logo-bg.png" alt="">
          </div>
        </div>
      </div>
    </div>

    <div class="socials-footer">
      <div class="container section-socials">
        <a class="button-sing" href="#">
          SIGN-UP NOW!
        </a>
        <div class="icons">
          <h4>FOLLOW US</h4>
          <div v-for="logo in brands">
            <img :src="'/img/' + logo.image" alt="">
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>


<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.socials-footer{
  background-color: $footer;
  padding: 40px 0;

  .section-socials{
    display: flex;
    justify-content: space-between;
    align-items: center;

    .button-sing{
      color: white;
      border: 4px solid $blue-color;
      padding: 5px;
    }

    .icons{
      display: flex;
      gap: 20px;
      align-items: center;
    }
  }

  h4{
    color: $blue-color;
    margin: 0;
    font-size: 20px;
  }
  .button {
        border: 1px solid $blue-color;
        padding: .5rem;
    }
}

.background-section{
  background-image: url('/img/footer-bg.jpg');
  object-fit: cover;

  .link-section{
    display: flex;
    gap: 50px;
    height: 400px;

    .link-col{
      display: flex;
      flex-direction: column;

      h3{
        color: white;
        padding-top: 20px;
        text-transform: uppercase;
      }

      a{
        text-decoration: none;
        color: gray;
      }
    }
  }

  .background-img{
    width: 100%;
    height: 100%;

  .logo-bg{
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
}
}
</style>