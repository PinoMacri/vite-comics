<script>
import "@fontsource/open-sans-condensed"
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}
</script>




<template>
    <header class="container">
        <div>
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div>
            <ul>
                <li v-for="link in links" v-bind:key="link.text">
                    <a v-bind:href="link.url">
                        <b>{{ link.text }}</b>
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>




<style lang="scss" scope>
@use "../assets/sass/mixin" as *;
@use "../assets/sass/variables" as *;

ul {
    @include style-list;
    @include between-flex;


    a {
        @include style-list;
        color: $text-color-black;
        text-transform: uppercase;
        margin: 0px 20px;

        &:hover {
            color: $text-color-blue;
        }
    }
}

header {
    @include between-flex;
    font-family: "Open Sans Condensed", sans-serif;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}
</style>
