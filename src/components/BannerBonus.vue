<script>
export default {
    name: "BannerBonus",
    data() {
        return {
            icons: [
                {
                    icon: '',
                },
                {
                    icon: '',
                },
                {
                    icon: '',
                },
                {
                    icon: '',
                },
                {
                    icon: '',
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

<template></template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss";
@use "../styles/partials/_mixins.scss";
</style>
