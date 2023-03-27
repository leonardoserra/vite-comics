<script>
export default {
    name: "Banner",
    data() {
        return {
            icons: [
                {
                    icon: 'footer-facebook.png',
                },
                {
                    icon: 'footer-twitter.png',
                },
                {
                    icon: 'footer-youtube.png',
                },
                {
                    icon: 'footer-pinterest.png',
                },
                {
                    icon: 'footer-periscope.png',
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
        <div class="wrapper">
            <button class="sign-up">SIGN-UP NOW</button>
        </div>
        <div class="wrapper">
            <h2>FOLLOW US</h2>
            <div class="socials">
                <img class="icon" v-for="(icon, i) in icons" :src="getImagePath(icon.icon)">
            </div>
        </div>


    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss";
@use "../styles/partials/_mixins.scss";

.container {
    height: 121px;
    background-color: variables.$secondary-color;
    @include mixins.flex-around;

    .wrapper {
        width: 30%;
    }

    .icon {
        margin-left: 15px;
    }
}
</style>
