<script>
export default {
    name: "TheHeader",
    data() {
        return {
            categories: [
                {
                    category: 'CHARACTERS',
                    href: '#'
                },
                {
                    category: 'COMICS',
                    href: '#'
                },
                {
                    category: 'MOVIES',
                    href: '#'
                },
                {
                    category: 'TV',
                    href: '#'
                },
                {
                    category: 'GAMES',
                    href: '#'
                },
                {
                    category: 'COLLECTIBLES',
                    href: '#'
                },
                {
                    category: 'VIDEOS',
                    href: '#'
                },
                {
                    category: 'FANS',
                    href: '#'
                },
                {
                    category: 'NEWS',
                    href: '#'
                },
                {
                    category: 'SHOP',
                    href: '#'
                }
            ]
        }
    }

}
</script>

<template>
    <div class="container">
        <img class="logo" src="../assets/img/dc-logo.png" alt="logo" />
        <nav class="navbar-menu">
            <ol class="categories">
                <li v-for="(links, i) in categories" :key="i"><a :href="'href'">{{ links.category }}</a>
                </li>
            </ol>
        </nav>
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

    .categories {
        @include mixins.flex-around;
        list-style: none;

        li {
            padding: 20px;

            a {
                display: inline-block;
                height: 80px;
                line-height: 80px;
                color: variables.$secondary-color;
                text-decoration: none;

                &:hover {
                    color: variables.$tertiary-color;
                    border-bottom: 5px solid lighten(variables.$tertiary-color, $amount: 15);
                    transition: color .5s ease, border-bottom .03s linear;
                }
            }
        }


    }
}
</style>
