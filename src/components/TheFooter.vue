<script>
export default {
    components: {

    },
    data() {
        return {
            DcComicsLinks: [
                { name: "Characters" },
                { name: "Comics" },
                { name: "Movies" },
                { name: "Tv" },
                { name: "Games" },
                { name: "Videos" },
                { name: "News" },
            ],
            ShopLinks: [
                { name: "Shop Dc" },
                { name: "Shop Collectables" },
            ],
            DCLinks: [
                { name: "Terms Of Use" },
                { name: "Privacy Policy(New)" },
                { name: "AdChoice" },
                { name: "Advertising" },
                { name: "Jobs" },
                { name: "Subscriptions" },
                { name: "Talent Workshops" },
                { name: "CPSC Certificates" },
                { name: "Ratings" },
                { name: "Shop Help" },
                { name: "Contact Us" },
            ],
            SitesLinks: [
                { name: "DC" },
                { name: "Mad Magazine" },
                { name: "DC Kids" },
                { name: "DC Universe" },
                { name: "DC Power Visa" },
            ],
        }
    }
}
</script>

<template>
    <footer>
        <div class="my-c-top">
            <div class="container">
                <div class="left-side">
                    <div class="pe-4">
                        <h4>DC COMICS</h4>
                        <ul class="list-unstyled">
                            <li v-for="link in DcComicsLinks">
                                <a href="#0">{{ link.name }}</a>
                            </li>
                        </ul>
                        <h4>SHOP</h4>
                        <ul class="list-unstyled">
                            <li v-for="link in ShopLinks">
                                <a href="#0">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="pe-4">
                        <h4>DC</h4>
                        <ul class="list-unstyled">
                            <li v-for="link in DCLinks">
                                <a href="#0">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h4>SITES</h4>
                        <ul class="list-unstyled">
                            <li v-for="link in SitesLinks">
                                <a href="#0">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="right-side">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="my-c-bot py-4">
            <div class="container">
                <button class="btn btn-outline-primary fw-bold">SING-UP NOW!</button>

                <div>
                    <h4>FOLLOW US</h4>
                    <a href="#0">
                        <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                    </a>
                    <a href="#0">
                        <img src="../assets/img/footer-twitter.png" alt="Twitter logo">
                    </a>
                    <a href="#0">
                        <img src="../assets/img/footer-youtube.png" alt="YouToube logo">
                    </a>
                    <a href="#0">
                        <img src="../assets/img/footer-pinterest.png" alt="Pinterest logo">
                    </a>
                    <a href="#0">
                        <img src="../assets/img/footer-periscope.png" alt="Periscope logo">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {
    .my-c-top {
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;

        >.container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: $text-color-secondary;
            height: 400px;

            >.left-side {
                display: flex;

                a {
                    font-size: .8rem;
                    color: gray;
                }
            }

            >.right-side {
                overflow: hidden;
                /* Nasconde le parti dell'immagine che eccedono il contenitore */
                display: flex;
                align-items: center;
                /* Centra verticalmente l'immagine */
                justify-content: center;
                /* Centra orizzontalmente l'immagine */
                height: 100%;
                /* Altezza uguale a quella del my-c-top */
                flex-shrink: 0;
                /* Evita il restringimento dell'immagine */
            }
        }
    }

    .my-c-bot {
        background-color: $color-secondary;

        >.container {
            display: flex;
            justify-content: space-between;

            div {
                display: flex;
                justify-content: space-around;
                align-items: center;

                >h4 {
                    margin: 0;
                    padding-right: 10px;
                    color: $color-primary;
                }

                a {
                    padding: 0 10px 0 10px;
                }
            }
        }
    }

    button {
        color: $text-color-secondary;
        border-radius: 0;
        padding: .7rem;
        border: 3px solid $color-primary;
    }

    a {
        text-decoration: none;
    }
}</style>