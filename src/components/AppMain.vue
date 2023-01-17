<script>
import ComicsCard from './ComicsCard.vue'
import Comics from './data/Comics.js'
export default {
    name: 'SiteMain',
    components: {
        ComicsCard
    },
    data() {
        return {
            cards: [
                {
                    image: 'buy-comics-digital-comics.png',
                    text: 'digital comics'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    text: 'dc merchandise'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    text: 'subscription'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    text: 'comic shop location'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    text: 'dc power visa'
                }
            ],
            comics: Comics
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
}
</script>


<template>
    <div class="jumbotron">
    </div>
    <div class="shop">
        <div class="container">
            <div class="banner-top">
                <h5>current series</h5>
            </div>
            <div class="cards">
                <ComicsCard v-for="comic in comics" :url="comic.thumb" :title="comic.series" />
            </div>
            <div class="load">
                <button class="btn-load">Load more</button>
            </div>
        </div>
    </div>
    <div class="banner">
        <div class="container">
            <div class="icons">
              <div class="blue-section-items" v-for="card in cards">
                <img :src="'/img/' + card.image" alt="">
                <p>{{ card.text }}</p>
            </div>
          </div>
        </div>
    </div>
</template>


<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.jumbotron {
        background-image: url('/img/jumbotron.jpg');
        background-size: cover;
        height: 40vh;
}

.shop {
    background-color: $dark;
    padding: 3rem 0 2rem 0;

    .banner-top {
        color: white;
        text-transform: uppercase;
        background-color: $blue-color;
        width: 12rem;
        padding: 1rem .5rem 1rem 1rem;
        position: relative;
        top: -4.3rem;

        h5{
          text-align: center;
        }
    }

    .cards{
        display: flex;
        flex-wrap: wrap;
        gap: 30px;
    }

    .load {
        display: flex;
        justify-content: center;

        .btn-load {
            color: white;
            background-color: $blue-color;
            padding: 10px;
            margin-top: 10px;
        }
    }
}

.banner {
    background-color: $blue-color;

    .icons{
        display: flex;
        gap: 10px;

        .blue-section-items{
            display: flex;
            align-items: center;

            img {
                width: 40px;
                height: 50px;
                margin: 3rem 1rem;
            }

            p {
                color: white;
                text-transform: uppercase;
            }
        }
    }
}
</style>