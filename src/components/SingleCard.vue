<script>
export default {
    name: "SingleCard",
    app() {
        return {

        }
    },
    props: {
        thumb: String,
        series: String
    }
}

</script>

<template>
    <div class="wrapper">
        <img :src="thumb" :alt="series">
        <div class="title">{{ series }}</div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/_mixins.scss";
@use "../styles/partials/_variables.scss" as*;


.wrapper {
    height: calc(100% / 2 - 20px);
    margin: 10px;
    width: calc(100% / 6 - 20px);
    background-color: white;

    img {
        margin-bottom: 5px;
        width: 100%;
    }

    .title {
        color: $primary-color;
    }
}
</style>