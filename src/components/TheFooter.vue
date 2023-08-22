<script>
export default {
    components: {

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
                            <li><a href="#0">Characters</a></li>
                            <li><a href="#0">Comics</a></li>
                            <li><a href="#0">Movies</a></li>
                            <li><a href="#0">TV</a></li>
                            <li><a href="#0">Games</a></li>
                            <li><a href="#0">Videos</a></li>
                            <li><a href="#0">News</a></li>
                        </ul>
                        <h4>SHOP</h4>
                        <ul class="list-unstyled">
                            <li><a href="#0">Shop DC</a></li>
                            <li><a href="#0">Shop DC Collectibles</a></li>
                        </ul>
                    </div>
                    <div class="pe-4">
                        <h4>DC</h4>
                        <ul class="list-unstyled">
                            <li><a href="#0">Terms Of Use</a></li>
                            <li><a href="#0">Privacy policy (New)</a></li>
                            <li><a href="#0">Ad Choise</a></li>
                            <li><a href="#0">Advertising</a></li>
                            <li><a href="#0">Jobs</a></li>
                            <li><a href="#0">Subscriptions</a></li>
                            <li><a href="#0">Talent Workshops</a></li>
                            <li><a href="#0">CPSC Certification</a></li>
                            <li><a href="#0">Ratings</a></li>
                            <li><a href="#0">Shop Help</a></li>
                            <li><a href="#0">Contact Us</a></li>
                        </ul>
                    </div>
                    <div>
                        <h4>SITES</h4>
                        <ul class="list-unstyled">
                            <li><a href="#0">DC</a></li>
                            <li><a href="#0">MAD Magazine</a></li>
                            <li><a href="#0">DC Kids</a></li>
                            <li><a href="#0">DC Univers</a></li>
                            <li><a href="#0">DC Power Visa</a></li>
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

            >.left-side {
                display: flex;

                a {
                    font-size: .8rem;
                    color: gray;
                }
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
}
</style>