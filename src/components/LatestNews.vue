<template>
    <div class="content-container margin-bottom-cs margin-top-cs">
        <div class="row ">
            <div class="col-12 text-uppercase text-center">
                <p>Pelicula Studio</p>
                <h1 class="fw-bold">THIS IS WHAT WE DO</h1>
            </div>
        </div>

        <div class="row flex-nowrap overflow-auto">
            <div v-for="item in dataListPelicula" class="col-4">
                <img :src="getImagePath(item.image)" alt="Image of pelicula" class="mb-3">
                <span class="date">{{ item.date }}</span>
                <h6 class="my-3 fw-bold text-uppercase">{{ item.title }}</h6>
                <p>{{ item.text }}</p>
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
                    image: 'blog07.jpg',
                    date: 'November 06 , 2021 By Admin',
                    title: 'RECAP YOUR LATEST COMPANY EVENT',
                    text: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog06.jpg',
                    date: 'May 27 , 2022 By Admin',
                    title: 'How To Edit A Film Score To Serve',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut',
                },
                {
                    image: 'blog05.jpg',
                    date: 'May 07 , 2022 By Admin',
                    title: 'ARE YOU READY TO MAKE IT AWESOME',
                    text: 'Design is our playground. While we create an awesome experience, we like having fun. No animals',
                },
                {
                    image: 'blog04.jpg',
                    date: 'April 10 , 2022 By Admin',
                    title: 'LAST VIDEO WEBSITE YOU NEED FOR',
                    text: 'In as name to here them deny wise this. As rapid woody my he me which. Men but they fail shew just Band uprising to cult status',
                },
                {
                    image: 'blog03.jpg',
                    date: 'March 01 , 2022 By Admin',
                    title: 'BAND UPRISING TO CULT STATUS',
                    text: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog02.jpg',
                    date: 'November 06 , 2021 By Admin',
                    title: 'RECAP YOUR LATEST COMPANY EVENT',
                    text: 'Porta tellus aliquam ligula sollicitudin Tincidunt habitant egestas erat lectus congue nisl Bringing the stage to life',
                },
                {
                    image: 'blog01.jpg',
                    date: 'February 14 , 2022 By Admin',
                    title: 'BRINGING THE STAGE TO LIFE',
                    text: 'Actor The Concept Movie High Concept Theory see the post As Clover Letter Emails Got Cadenze rios picked for the Next picture',
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
        margin: 0;
    }

    p,
    span {
        color: $ColorGray;
    }
}
</style>