<template>
    <div class="content-container">
        <div class="row margin-top-cs">
            <div class="col-12 text-uppercase text-center">
                <p>Your WatchList</p>
                <h1 class="fw-bold">Best Hits Movie</h1>
            </div>
        </div>

        <div class="row">
            <div v-for="item in dataWatchList" class="col-4 text-center">
                <img :src="getImagePath(item.image)" alt="Image of pelicula" class="mb-5">
                <h6>{{ item.title }}</h6>
                <p>{{ item.text }}</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataWatchList: [
                {
                    title: "SEVENTEENTH SUMMER",
                    image: "Gallery-01.jpg",
                    text: "Commercial, Music Video.",
                },
                {
                    title: "A MESSAGE TO SPACE",
                    image: "Gallery-02.jpg",
                    text: "Short Film",
                },
                {
                    title: "THE MOST BEAUTIFUL THING",
                    image: "Gallery-03.jpg",
                    text: "Music Video",
                },
                {
                    title: "PERMISSION TO SPEAK",
                    image: "Gallery-04.jpg",
                    text: "Documentary",
                },
                {
                    title: "EXPLORE OUR SPACE",
                    image: "Gallery-05.jpg",
                    text: "Film noir",
                },
                {
                    title: "FILM PRODUCTION",
                    image: "Gallery-06.jpg",
                    text: "Blaxploitation",
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

div.col-12 {
    color: $ColorBlack;

    h1 {
        margin-top: $marginTopPellicula;
    }
}

div.col-4 {
    margin-top: $marginTopPellicula;

    img {
        width: 100%;
    }

    p {
        font-size: 17px;
        color: $ColorGray;
    }
}
</style>