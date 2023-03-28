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
    <div class="card">
        <div class="img-container">
            <img :src="thumb" :alt="series">
        </div>
        <div class="title">{{ series }}</div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/_mixins.scss";
@use "../styles/partials/_variables.scss" as*;


.card {
    width: calc(100vw / 6 - 10px);
    height: calc(100vw / 6);

    .img-container {
        height: 100%;
        width: 100%;
        padding: 15px;

        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }

    }

    .title {
        color: $primary-color;
    }
}
</style>