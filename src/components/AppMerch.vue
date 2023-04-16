<script>
export default {
    name: "AppMerch",
    data() {
        return {
            merch: [
                {
                    name: "DIGITAL COMICS",
                    img: "buy-comics-digital-comics.png",
                    url: "#"
                },
                {
                    name: "DV MERCHANDISE",
                    img: "buy-comics-merchandise.png",
                    url: "#"
                },
                {
                    name: "SUBSCRIPTION",
                    img: "buy-comics-subscriptions.png",
                    url: "#"
                },
                {
                    name: "COMIC SHOP LOCATOR",
                    img: "buy-comics-shop-locator.png",
                    url: "#"
                },
                {
                    name: "DC POWER VISA",
                    img: "buy-dc-power-visa.svg",
                    url: "#"
                },
            ]
        }
    },
    methods: {

        getImgPath(item) {
            return new URL(`../assets/img/${item.img}`, import.meta.url).href;
        }
    }
}
</script>


<!-- GENERETE LAYOUT  -->
<template>
    <div class="merch">
        <div class="merch-container">
            <ul>
                <li v-for="merch in merch">
                    <a :href="merch.url">
                        <img :src="getImgPath(merch)" alt="">
                        <p>{{ merch.name }}</p>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>


<!-- STYLE LAYOUT  -->
<style scoped lang="scss">
@use "./style/partials/mixins" as *;
@use "./style/partials/variables" as *;
.merch {
    background-color: $primary;
    height: 170px;
    margin: 0 auto;
    position: relative;
    z-index: 10;
    .merch-container {
        margin: 0 auto;
        width:80% ;
        ul {
            @include flex(row, space-between, center);
            list-style: none;
            height: 170px;
            li {
                color: white;
                a {
                    @include flex(row, space-between, center);
                    text-decoration: none;
                    font-weight: 700;
                    color: inherit;
                    font-size: 1rem;
                    img {
                        width: 50px;
                        padding: 5px;
                    }
                }
            }
        }
    }
}
</style>