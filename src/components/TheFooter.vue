<script>
export default {
    name: "TheFooter",
    data() {
        return {
            categories: [
                {
                    category: 'DC COMICS',
                    links: ['Characters', 'Comic', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    category: 'SHOP',
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    category: 'DC',
                    links: ['Terms Of Use', 'Privacy policy(New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    category: 'SITES',
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                }
            ]
        }
    }

}

</script>

<template>
    <div class="container">
        <div class="links-wrapper">
            <div class="footer-links">
                <div class="category" v-for="(category, i) in categories" :key="i">
                    <h3>{{ category.category }}</h3>
                    <ul>
                        <li v-for="(links, c) in category.links"><a :href="category.links[c]">{{ category.links[c] }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="img-wrapper">
            <img class="logo-bg" src="../assets/img/dc-logo-bg.png" alt="logo-bg" />
        </div>
    </div>
</template>

<style  lang="scss" scoped>
@use "../styles/partials/_variables.scss";
@use "../styles/partials/_mixins.scss";

.container {
    overflow-y: hidden;
    height: 300px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    @include mixins.flex-around;

    .links-wrapper {
        height: 100%;
        margin-top: 45px;
        width: 40%;

        .footer-links {
            @include mixins.flex-columns;
            height: 100%;
            margin: 0 20px;
            padding: 30px;

            .category {
                margin: 0 20px;
                margin-bottom: 20px;
                color: variables.$primary-color;


                li {
                    list-style: none;

                    a {
                        font-size: 10px;
                        color: lighten(variables.$secondary-color, $amount: 10);
                        text-decoration: none;

                        &:hover {
                            color: lighten(variables.$secondary-color, $amount: 30);
                            border-bottom: 1px solid lighten(variables.$tertiary-color, $amount: 10);
                            transition: border-bottom 0.5s linear;
                            transition: color .5s linear;
                        }
                    }
                }
            }
        }


    }

    .logo-bg {
        height: 390px;
    }


}
</style>
