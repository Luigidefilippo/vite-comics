<script>
export default {
    name: "AppFooter",
    data() {
        return {
            links: {
                // SECTION FOR ALL PART OF FOOTER
                "DC COMICS": [
                    {
                        name: "Characters",
                        url: "#"
                    },
                    {
                        name: "Comics",
                        url: "#"
                    },
                    {
                        name: "Movies",
                        url: "#"
                    },
                    {
                        name: "TV",
                        url: "#"
                    },
                    {
                        name: "Games",
                        url: "#"
                    },
                    {
                        name: "Videos",
                        url: "#"
                    },
                    {
                        name: "News",
                        url: "#"
                    }
                ],

                "DC": [
                    {
                        name: "Terms Of Use",
                        url: "#"
                    },
                    {
                        name: "Privacy policy(New)",
                        url: "#"
                    },
                    {
                        name: "Ad Choices",
                        url: "#"
                    },
                    {
                        name: "Advertising",
                        url: "#"
                    },
                    {
                        name: "Jobs",
                        url: "#"
                    },
                    {
                        name: "Subscriptions",
                        url: "#"
                    },
                    {
                        name: "Talet Workshops",
                        url: "#"
                    },
                    {
                        name: "CPSC Certificates",
                        url: "#"
                    },
                    {
                        name: "Ratings",
                        url: "#"
                    },
                    {
                        name: "Shop Help",
                        url: "#"
                    },
                    {
                        name: "Contact Us",
                        url: "#"
                    }
                ],

                "SITES": [
                    {
                        name: "DC",
                        url: "#"
                    },
                    {
                        name: "MAD Magazine",
                        url: "#"
                    },
                    {
                        name: "DC Kids",
                        url: "#"
                    },
                ],

                "SHOP": [
                    {
                        name: "Shop DC",
                        url: "#"
                    },
                    {
                        name: "Shop DC Collectibles",
                        url: "#"
                    }
                ],
            }
        }
    }
}
</script>



<template>
    <footer>
    <div class="footer-all">
        <div class="footer-container">
            <div class="footer-top">
                <div class="row">
                    <div class="col" v-for="(item, key) in links">
                        <h3>{{ key }}</h3>
                        <ul>
                            <li v-for="link in item">
                                <a :href="link.url">
                                    {{ link.name }}
                                </a>
                            </li>
                        </ul>
                    </div>

                </div>

            </div>
            <div class="footer-top-img">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
    <div class="footer-down">
            <div class="container">
                <div class="sign-up">
                    <a href="#">SIGN-UP NOW!</a>
                </div>
                <div class="links">
                    <h3>FOLLOW US</h3>
                    <ul>
                        <li v-for="img in social">
                            <a :href="img.url">
                            <img :src="getImagePath(img)" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "./style/partials/mixins" as *;
@use "./style/partials/variables" as *;

.footer-all {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    .footer-container {
        display: flex;
        flex-direction: row;
        width: 70%;
        margin: 0 auto;
        position: relative;

        .footer-top {
            height: 400px;
            display: flex;
            justify-content: center;
            flex-direction: column;

            .row {
                display: flex;
                flex-wrap: wrap;
                .col {
                    width: calc(100% / 3);
                    h3 {
                        color: white;
                    }
                    ul {
                        li {
                            display: flex;
                            padding: 3px 0;
                            a {
                                text-decoration: none;
                                color: lightgrey;
                            }
                        }
                    }
                }
            }
        }
        .footer-top-img {
            img {
                max-width: 80%;
                position: absolute;
                top: -60px;
            }
        }
    }
}
.footer-down {
        position: relative;
        z-index: 1;
        height: 100px;
        background-color: #303030;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 80%;
            margin: 0 auto;
            .sign-up {
                a {
                    color: inherit;
                    color: white;
                    text-decoration: none;
                    padding: 8px;
                    border: 2px solid #0082f9;
                }
            }
        }
    }
</style>