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

    .img-container {
        height: 90%;
        width: 90%;
        padding: 15px;

        img {
            height: 90%;
            width: 90%;
            object-fit: cover;
        }

    }

    .title {
        padding: 0 15px;
        color: $primary-color;
    }
}
</style>