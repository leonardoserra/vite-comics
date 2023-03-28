<script>
export default {
    name: "BannerBonus",
    data() {
        return {
            items: [
                {
                    icon: 'buy-comics-digital-comics.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    icon: 'buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE'
                },
                {
                    icon: 'buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION'
                },
                {
                    icon: 'buy-comics-shop-locator.png',
                    title: 'COMIC SHOP LOCATOR'
                },
                {
                    icon: 'buy-dc-power-visa.svg',
                    title: 'DC POWER VISA'
                }
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="card" v-for="(card, i) in items" :key="i">
            <img :src="getImagePath(card.icon)" :alt="card.title" />
            <a :href="card.title">
                <h4 class="title">{{ card.title }}</h4>
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/_mixins.scss";

.container {
    height: 120px;
    background-color: $tertiary-color;
    @include mixins.flex-center;

    .card {
        height: 100%;
        @include mixins.flex-center;
        margin: 0 35px;
        color: $primary-color;


        &:last-child img {
            height: 20%;
        }

        img {
            height: 30%;
        }

        a {
            margin-left: 5px;
            text-decoration: none;
            color: $primary-color;

            .title {
                font-size: .7rem;
                font-weight: 400;
            }

        }
    }
}
</style>
