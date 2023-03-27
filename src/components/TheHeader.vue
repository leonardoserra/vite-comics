<script>
export default {
    data() {
        return {
            navbarSections: [
                {
                    category: 'CHARACTERS'
                },
                {
                    category: 'COMICS'
                },
                {
                    category: 'MOVIES'
                },
                {
                    category: 'TV'
                },
                {
                    category: 'GAMES'
                },
                {
                    category: 'COLLECTIBLES'
                },
                {
                    category: 'VIDEOS'
                },
                {
                    category: 'FANS'
                },
                {
                    category: 'NEWS'
                },
                {
                    category: 'SHOP'
                }
            ]
        }
    }

}
</script>

<template>
    <div class="container">
        <img class="logo" src="../assets/img/dc-logo.png" alt="logo" />
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss";
@use "../styles/partials/_variables.scss";

.container {
    @include mixins.flex-around;
    height: 80px;
    padding: 10px 0;
    background-color: variables.$primary-color;


    .logo {
        height: 100%;
    }
}
</style>
