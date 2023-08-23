<script>
export default {

}
</script>

<template>
    <div class="comics-section">
        <div class="container my-5">
            <div class="row gy-4">
                <div class="col-2">
                    <div class="card">
                        <img src="../assets/img/dc-logo.png" class="card-img-top" alt="">
                        <div class="card-body">
                            <h5 class="card-title">Card title</h5>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.comics-section {
    .card {
        background-color: #1C1C1C !important;
        color: $text-color-secondary;
        border: 0;

        img {
            width: 100%;
        }
    }
}
</style>