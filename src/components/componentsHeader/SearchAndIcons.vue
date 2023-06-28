<template>
    <div class="social d-flex align-items-center justify-content-between">
        <div class="search me-4 ">
            <img class="svg" src="../../assets/image (8).svg" alt="">
        </div>
        <div class="social-icons d-flex align-items-center">
            <i class="fa-brands fa-facebook-f me-4 svg"></i>
            <img class="me-4 svg" src="../../assets/image (10).svg" alt="">
            <img class="me-4 svg" src="../../assets/image (11).svg" alt="">
            <img class="svg" src="../../assets/image (12).svg" alt="">
        </div>
    </div>
</template>
<script>
export default {

}
</script>
<style lang="scss">
@use "../../styles/utilities/variables.scss" as *;

.svg {
    transition: all .2s ease;
    cursor: pointer;
}

.svg:hover {
    filter: invert(50%);
}

div.search {
    padding-right: 20px;
    border-right: 1px solid #cccccc;
}

div.social-icons {
    i {
        font-size: 18px;
    }

    img {
        height: 18px;
        width: 18px;
    }
}
</style>