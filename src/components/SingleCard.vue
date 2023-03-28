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

    width: calc(100% / 6 - 10px);
    height: calc(80vw / 6 - 10px);
    margin: 5px;

    .img-container {
        height: 150px;
        width: 150px;
        margin-bottom: 5px;

        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }

    }

    .title {
        // padding: 0 15px;
        color: $primary-color;
    }
}
</style>