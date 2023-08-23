<script>
export default {
    components: {

    },
    data() {
        return {
            menuItems: [
                {
                    name: 'DIGITAL COMICS',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'digital comics img'
                },
                {
                    name: 'DC MERCHANDISE',
                    image: '../assets/img/buy-comics-merchandise.png',
                    alt: 'merchandise img'
                },
                {
                    name: 'SUBSCRIPTION',
                    image: '../assets/img/buy-comics-shop-locator.png',
                    alt: 'subscription img'
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    image: '../assets/img/buy-comics-subscriptions.png',
                    alt: 'shop locator img'
                },
                {
                    name: 'DC POWER VISA',
                    image: '../assets/img/buy-dc-power-visa.svg',
                    alt: 'power visa img'
                },
            ],
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`${img}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="my-navbar py-5">
        <div class="container">
            <ul>
                <li class="list-unstyled" v-for="(item, i) in menuItems" :key="`item_${i}`">
                    <a href="#0">
                        <img :src="getImagePath(item.image)" :alt='item.alt'>
                        {{ item.name }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.my-navbar {
    background-color: $color-primary;

    ul {
        display: flex;
        justify-content: space-around;
    }
}

img {
    height: 60px;
    padding-right: 10px;
}

a {
    color: $text-color-secondary;
    text-decoration: none;
    font-weight: bold;
    font-size: .8rem;
}
</style>