<template>
    <div class="content-container margin-bottom-cs  margin-top-cs">
        <div class="row ">
            <div class="col-12 text-uppercase text-center">
                <p>The pericuros</p>
                <h1 class="fw-bold">Meet the team</h1>
            </div>
        </div>

        <div class="row">
            <div v-for="item in dataWatchList" class="col-3 text-center">
                <figure>
                    <img :src="getImagePath(item.image)" alt="Image of pelicula" class="mb-3">
                </figure>
                <h6 class="fw-bold text-uppercase">{{ item.nameMember }}</h6>
                <p>{{ item.role }}</p>
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
                    nameMember: "Fabricio Guerra",
                    image: "Team-01.jpg",
                    role: "Main Director",
                },
                {
                    nameMember: "Umberto Pagoda",
                    image: "Team-02.jpg",
                    role: "Main Writer",
                },
                {
                    nameMember: "Gloria Riccasso",
                    image: "Team-03.jpg",
                    role: "Main Producer",
                },
                {
                    nameMember: "Lion Napoin",
                    image: "Team-04.jpg",
                    role: "Cameraman",
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

div.col-3 {
    margin-top: $marginTopPellicula;

    figure {
        width: 270px;
        height: 329.27px;
        overflow: hidden;
    }

    img {
        width: 100%;
        transition: all .2s ease;
    }

    img:hover {
        transform: scale(1.1);
    }

    h6 {
        letter-spacing: 0.6px;
    }

    p {
        font-size: 17px;
        color: $ColorGray;
    }
}
</style>