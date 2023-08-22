<script>
export default {
    components: {

    }
}
</script>

<template>
    <header>
        <div class="container py-4">
            <img src="../assets/img/dc-logo.png" alt="DC logo">

            <ul class="nav nav-pills">
                <li class="nav-imtem"><a href="#0" class="nav-link">CHARACTERS</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link active">COMICS</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">MOVIES</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">TV</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">GAMES</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">COLLECTIBLES</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">VIDEOS</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">FANS</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">NEWS</a></li>
                <li class="nav-imtem"><a href="#0" class="nav-link">SHOP</a></li>
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