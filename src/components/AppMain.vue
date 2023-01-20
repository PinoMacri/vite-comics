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
                { text: "comic shop locator ", img: "buy-comics-subscriptions.png" },
                { text: "subscription ", img: "buy-comics-shop-locator.png" },
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
                    <b> -- > Content goes here --</b>
                </p>
            </div>
        </div>
        <div id="listMain">
            <nav class="container">
                <ul>
                    <li v-for="image in images">
                        <p>{{ image.text }}</p>
                        <img :src=dinamicImg(image) alt="">
                    </li>
                </ul>
            </nav>
        </div>
    </main>
</template>

<style lang="scss" scope>
@use "../assets/sass/mixin" as *;
@use "../assets/sass/variables" as *;

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
}
</style>
