<template>
    <div class="content-container">
        <div class="row margin-top-cs">
            <div class="col-12 text-uppercase text-center">
                <p>Pelicula Studio</p>
                <h1 class="fw-bold">THIS IS WHAT WE DO</h1>
            </div>
        </div>

        <div class="row">
            <div v-for="item in dataListPelicula" class="col-4 text-center">
                <img :src="getImagePath(item.image)" alt="Image of pelicula" class="mb-5">
                <h4>{{ item.text }}</h4>
                <p>{{ item.lorem }}</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataListPelicula: [
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (14).svg",
                    text: "ARRAY OF EQUIPMENT",
                },
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (16).svg",
                    text: "NEW TECHNOLOGIES",
                },
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (18).svg",
                    text: "VERSITILE ACTORS",
                },
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (15).svg",
                    text: "TOP DIRECTORS",
                },
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (17).svg",
                    text: "MINUTE EDITING",
                },
                {
                    lorem: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
                    image: "image (19).svg",
                    text: "VERSITILE ACTORS",
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
        width: 80px;
        height: 80px;
    }

    p {
        color: $ColorGray;
    }
}
</style>