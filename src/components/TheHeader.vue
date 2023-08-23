<script>
export default {
    components: {

    },
    data() {
        return {
            navLinks: [
                { name: 'CHARACTER', },
                { name: 'COMICS', },
                { name: 'MOVIES', },
                { name: 'TV', },
                { name: 'GAMES', },
                { name: 'COLLECTIBLES', },
                { name: 'VIDEOS', },
                { name: 'FANS', },
                { name: 'NEWS', },
                { name: 'SHOP', },
            ],
        }
    },
}
</script>

<template>
    <header>
        <div class="container py-4">
            <a href="#0"><img src="../assets/img/dc-logo.png" alt="DC logo"></a>

            <ul class="nav nav-pills">
                <li class="nav-imtem" v-for="(link, i) in navLinks" :key="`link_${i}`">
                    <a href="#0" class="nav-link" :class="{ 'active': link.name === 'COMICS' }">{{ link.name }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
        width: 100px;
    }

    .nav-link {
        color: $text-color-primary;
        position: relative;
        border-radius: 0;

        &.active {
            color: $color-primary;
            font-weight: bold;
            background-color: transparent;
            border-bottom: 5px solid $color-primary;
        }
    }
}
</style>