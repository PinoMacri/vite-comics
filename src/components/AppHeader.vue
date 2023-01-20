<script>
import "@fontsource/open-sans-condensed"
export default {
    name: "AppHeader",
    data() {
        return {
            currentIndex: "Comics",
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

        <div class="divImgHeader">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <nav id="headerNav">

            <ul>
                <li v-for="link in links" v-bind:key="link.text" v-on:click="currentIndex = link.text">
                    <a class="principalLink" v-bind:href="link.url">
                        <b>{{ link.text }}</b>
                    </a>
                    <div v-if="currentIndex === link.text" class="selectedNav"></div>
                </li>
            </ul>

        </nav>

    </header>
</template>




<style lang="scss" scope>
@use "../assets/sass/mixin" as *;
@use "../assets/sass/variables" as *;



ul {
    @include style-list;
    @include between-flex;
    height: 100%;

    li {
        @include center-flex;
        flex-direction: column;
        width: calc(100% / 10);
        margin-left: 10px;
        position: relative;
        height: 100%;

        &:hover {
            cursor: pointer;

            a {
                color: $text-color-blue;
            }

        }
    }

    .principalLink {
        @include style-list;
        color: $text-color-black;
        text-transform: uppercase;
        margin: 0px 20px;



    }
}

.selectedNav {
    width: 100%;
    height: 7px;
    background-color: $text-color-blue;
    position: absolute;
    bottom: 0;

}

header {
    @include between-flex;
    font-family: "Open Sans Condensed", sans-serif;
    position: relative;
    height: 130px;

    .divImgHeader {
        display: flex;
        align-items: center;

    }
}

nav {
    height: 100%;
    @include center-flex
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}
</style>
