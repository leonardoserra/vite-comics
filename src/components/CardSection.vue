<script>
import SingleCard from "./SingleCard.vue";


export default {
    name: "CardSection",

    components: {
        SingleCard
    },

    data() {
        return {
            comics: [
                {
                    "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]

        }
    }
}
</script>


<template>
    <div class="wrapper">
        <div class="current-series">
            <h2>CURRENT SERIES</h2>
        </div>
        <div class="container">
            <SingleCard v-for="(comic, i) in comics" :key="i" :thumb="comic.thumb" :series="comic.series" />
            <button class="load-more">LOAD MORE</button>
        </div>
    </div>
</template>


<style scoped lang="scss">
@use "../styles/partials/_mixins.scss";
@use "../styles/partials/_variables.scss" as*;

.wrapper {
    height: 580px;
    position: relative;

    .current-series {
        font-size: 0.8rem;
        position: absolute;
        top: -20px;
        left: 20%;
        @include mixins.blue-text-white;

    }

    .load-more {
        @include mixins.blue-text-white;
        height: 30px;
        width: 200px;
        position: absolute;
        bottom: 20px;
        left: 50%;
        border: none;
        transform: translateX(-50%);

        &:hover {
            box-shadow: 0 0 25px rgb(166, 166, 166);
            transition: box-shadow 0.3s ease-in-out;

        }

        &:active {
            transition: background-color 0.2s ease-in-out;
            background-color: lighten($tertiary-color, $amount: 15);
        }
    }

    .container {
        @include mixins.flex-center-wrap;
        padding-top: 50px;
        width: 80vw;
        height: 100%;
        margin: auto;

    }
}
</style>