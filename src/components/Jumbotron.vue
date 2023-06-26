<template>
    <div class="jumbotron">
        <div class="content-container  d-flex align-items-center h-100">
            <div class="content text-uppercase">
                <p>Cinemato Studio</p>
                <h1 class="fw-bold">Action And Inspire People</h1>
                <button class="btn btn-light text-uppercase fw-bold">Read more</button>
            </div>
        </div>
    </div>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

div.jumbotron {
    height: 900px;
    width: 100%;
    background-image: url(../assets/blog01.jpg);
    background-size: cover;
    color: $ColorWhite;
    font-weight: bolder;
    line-height: 69px;

    h1 {
        width: 547px;
        font-size: 61px;
        margin: 0;

    }

    p {
        font-size: 16px;
        margin: 0;
    }

    button {
        border-radius: 0;
        font-size: 12px;
        padding: 9px 30px;
    }
}
</style>