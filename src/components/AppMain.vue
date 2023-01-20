<script>
import "@fontsource/open-sans"
export default {
    name: "AppMain",
    data() {
        return {
            currentIndex: "Comics",
            images: [
                { text: "digital comics ", img: "buy-comics-digital-comics.png" },
                { text: "dc merchandise ", img: "buy-comics-merchandise.png" },
                { text: "subscription ", img: "buy-comics-subscriptions.png" },
                { text: "comic shop locator ", img: "buy-comics-shop-locator.png" },
                { text: "dc power visa ", img: "buy-dc-power-visa.svg" },
            ]
        }
    }, methods: {
        dinamicImg(image) {
            const url = new URL(`../assets/img/${image.img}`, import.meta.url)
            return url.href
        }
    }
}
</script>




<template>
    <main>
        <div id="contentGoes">
            <div class="container">
                <p>
                    <b>-- Content goes here --</b>
                </p>
            </div>
        </div>

        <div id="listMain">
            <nav class="container">
                <ul>
                    <li v-for="image in images">
                        <div id="containerList">
                            <div class="imgList">
                                <img :src=dinamicImg(image) alt="">
                            </div>
                            <div class="textList">
                                <p>{{ image.text }}</p>
                            </div>
                        </div>
                    </li>
                </ul>
            </nav>
        </div>
    </main>
</template>




<style lang="scss" scope>
@use "../assets/sass/mixin" as *;
@use "../assets/sass/variables" as *;

main {
    font-family: "Open Sans Condensed", sans-serif;
}

#contentGoes {
    display: flex;
    align-items: center;
    height: 110px;
    font-family: "Open Sans ", sans-serif;
    color: white;
    background-color: $text-color-black;
    font-size: $font-size;

    div {
        width: 100%;
    }
}

#listMain {
    height: 110px;
    background-color: $text-color-blue;

    ul {
        @include between-flex;
        width: 100%;
    }

    li {
        margin: 0;
        width: 20%;
        text-transform: uppercase;
        font-weight: bold;
        color: white;

        &:hover {
            cursor: default;
        }

        #containerList {
            display: flex;
            height: 100%;
            width: 100%;

            .imgList {
                display: flex;
                align-items: center;

                img {
                    height: 60%;
                    width: 100%;
                }
            }

            .textList {
                width: 70%;
                display: flex;
                align-items: center;
                margin-left: 10px
            }
        }
    }
}

nav {
    @include between-flex;
}
</style>
