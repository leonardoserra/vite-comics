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
        <div class="card" v-for="card in items">
            <img :src="card.icon" />
            <h4 class="title">{{ card.title }}</h4>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/_mixins.scss";

.container {
    height: 100px;
    background-color: $tertiary-color;
    @include mixins.flex-center;

    .card {
        margin: 0 35px;
        color: $primary-color;

        .title {
            font-size: .7rem;
            font-weight: 400;
        }
    }
}
</style>
