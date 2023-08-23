<script>
export default {
    props: {
        imgSrc: String,
        series: String
    }
}
</script>

<template>
    <div class="card">
        <a href="#0">
            <div class="img-container">
                <img :src="imgSrc" class="card-img" alt="">
            </div>
            <div class="card-body">
                <h5 class="card-title">{{ series }}</h5>
            </div>
        </a>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.card {
    background-color: #1C1C1C !important;
    border: 0;

    a {
        text-decoration: none;
        color: $text-color-secondary;
    }
    .img-container {
        height: 200px;
        overflow: hidden;
    }

    .card-body {
        padding-left: 0;
    }
}
</style>