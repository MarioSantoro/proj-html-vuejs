<template>
    <div class="background parallax">
        <div class="container-icons content-container">
            <div class="content d-flex justify-content-between align-items-center">
                <div v-for="icon in dataIconsList" class="icons">
                    <img :src="getImagePath(icon.image)" alt="icons image">
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataIconsList: [
                {
                    image: '01.png'
                },
                {
                    image: '02.png'
                },
                {
                    image: '03.png'
                },
                {
                    image: '04.png'
                },
                {
                    image: '05.png'
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        },
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

div.background {
    background-image: url(../assets/Parallax-03.jpg);
    background-size: cover;
    background-position: center;

    div.container-icons {
        padding: 98px 0;
        color: $ColorWhite;
        font-weight: bold;

        span {
            font-size: 55px;
        }

        h6 {
            font-size: 17px;
            font-weight: bold;
        }
    }
}
</style>