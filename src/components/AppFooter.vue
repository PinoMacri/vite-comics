<script>
import "@fontsource/open-sans"
export default {
    name: "AppFooter",
    data() {
        return {
            linksComics: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News",
            ],
            linksShops: [
                "Shop DC",
                "Shop DC Collectibles",
            ],
            linksDC: [
                "Terms Of Use",
                "Privacy policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact Us"
            ],
            sites: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ]
        }
    }
}
</script>




<template>
    <footer>
        <div id="backgroundFooter">
            <div class="container ctnFooter">

                <div class="listeFooter">
                    <div>
                        <h3>DC COMICS</h3>
                        <ul class="listNavFooterComics">
                            <li v-for="linkComics in linksComics "><a href="#">{{ linkComics }}</a> </li>
                        </ul>
                        <h3>SHOP</h3>
                        <ul class="listNavFooterShop">
                            <li v-for="linkShop in linksShops "> <a href="#">{{ linkShop }}</a> </li>
                        </ul>
                    </div>
                    <div>
                        <h3>DC</h3>
                        <ul class="listNavFooterDC">
                            <li v-for="linkDC in linksDC"><a href="#">{{ linkDC }}</a></li>
                        </ul>
                    </div>
                    <div>
                        <h3>SITES</h3>
                        <ul class="listNavFooterSites">
                            <li v-for="site in sites"><a href="#">{{ site }}</a></li>
                        </ul>
                    </div>
                </div>
                <div class="imgFooter">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>

            </div>
        </div>
        <div id="lastSection">
            <div class="container">
                <button>SIGN-UP NOW!</button>
                <nav>

                    <h3>FOLLOW US</h3>
                    <ul>
                        <li><a class="loghiSocial" href="#"><img src="../assets/img/footer-facebook.png" alt=""></a>
                        </li>
                        <li><a class="loghiSocial" href="#"><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                        <li><a class="loghiSocial" href="#"><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                        <li><a class="loghiSocial" href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a>
                        </li>
                        <li><a class="loghiSocial" href="#"><img src="../assets/img/footer-periscope.png" alt=""></a>
                        </li>
                    </ul>

                </nav>
            </div>
        </div>
    </footer>
</template>




<style lang="scss" scope>
@use "../assets/sass/mixin" as *;
@use "../assets/sass/variables" as *;

footer {
    font-family: "Open Sans ", sans-serif;
    height: calc(100vh - 350px);
    border: 1px solid black;

    #backgroundFooter {
        height: 80%;
        background-image: url("../assets/img/footer-bg.jpg");
        background-size: cover;

        h3 {
            color: white;
        }

        .ctnFooter {
            height: 100%;
            display: flex;
            justify-content: space-between;
        }

        .listeFooter {
            display: flex;
            height: 100%;
            padding-top: 80px;

            .listNavFooterComics li {
                margin: 1px 0px;
            }

            .listNavFooterShop li {
                margin: 1px 0px;
            }

            .listNavFooterDC li {
                margin-bottom: 1px 0px;
            }

            .listNavFooterSites li {
                margin: 1px 0px;
            }

            div {
                max-height: 200px;
                margin-right: 50px;


                h3 {
                    padding: 10px 0px;
                }

            }
        }

        ul {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
            font-size: 12px;



            li {
                width: auto;
                margin: 0;
                cursor: default;
                height: 20px;
                margin: 5px 0px;

                a {
                    @include style-list;
                    color: $text-color-black;
                    color: rgb(155, 155, 155);

                    &:hover {
                        text-decoration: underline;
                    }
                }

            }


        }

        .imgFooter {
            height: 100%;
            overflow: hidden;
        }

        .imgFooter img {
            object-fit: cover;
            object-position: 0px -70px;
            width: 700px;
            height: 700px;
        }
    }

    #lastSection {

        background-color: $text-color-black;
        height: 20%;

        div.container {
            @include between-flex;
            height: 100%;

            button {
                color: white;
                font-weight: bold;
                font-size: 18px;
                padding: 10px;
                background-color: transparent;
                border: 2px solid $text-color-blue;
                cursor: pointer;

                &:hover {
                    background-color: $text-color-blue ;
                }
            }
        }

        nav h3 {
            margin-right: 10px;
            color: $text-color-blue ;
        }
    }

    .loghiSocial {
        &:hover {
            transform: scale(1.3);
            color: white;
        }
    }
}
</style>
