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
            <div class="socials">
                <h2>FOLLOW US</h2>
                <a href=""><img class="icon" v-for="(icon, i) in icons" :src="getImagePath(icon.icon)"></a>
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
        width: 100%;
        @include mixins.flex-around;

        .socials {
            @include mixins.flex-start;
        }


        .sign-up {
            background-color: transparent;
            border: 3px solid variables.$tertiary-color;
            color: variables.$primary-color;
            height: 80%;
            padding: 20px;

            &:hover {
                background-color: lighten(variables.$secondary-color, $amount: 10);
                transition: background-color 0.5s ease-in-out;
            }

            &:active {
                background-color: lighten(variables.$tertiary-color, $amount: 10);
                transition: background-color 0.5s ease-in-out;
            }

            cursor: pointer;
        }

        h2 {
            color: variables.$tertiary-color;
            font-size: 18px;
        }
    }

    .icon {
        margin-left: 15px;
    }
}
</style>
