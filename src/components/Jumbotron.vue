<template>
    <div class="jumbotron">
        <img class="jumbo-image" :src="getImagePath(dataListJumbo[ActiveIndex].image)" alt="">
        <div class="content-container  d-flex align-items-center h-100">
            <div class="slider-button prev" @click="PreviousImage">
                <img src="../assets/left-arrow.svg" alt="">
            </div>
            <div class="slider-button next" @click="NextImage">
                <img src="../assets/right-arrow.svg" alt="">
            </div>
            <div class="content text-uppercase">
                <p>{{ dataListJumbo[ActiveIndex].type }}</p>
                <h1 class="fw-bold">{{ dataListJumbo[ActiveIndex].title }}</h1>
                <button class="btn btn-light text-uppercase fw-bold">Read more</button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataListJumbo: [
                {
                    image: 'Main-Banner-1.jpg',
                    type: 'Cinemato Studio',
                    title: 'Action And Inspire People'
                },
                {
                    image: 'Main-Banner-2.jpg',
                    type: 'Cinemato Director',
                    title: 'Dancing with of the stars'
                }
            ],
            ActiveIndex: 0,
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        },

        PreviousImage() {
            if (this.ActiveIndex === 0) {
                this.ActiveIndex = this.dataListJumbo.length - 1;
            } else {
                this.ActiveIndex--;
            }

        },

        NextImage() {
            if (this.ActiveIndex === this.dataListJumbo.length - 1) {
                this.ActiveIndex = 0;
            } else {
                this.ActiveIndex++;
            }

        },
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

div.jumbotron {
    position: relative;
    height: 900px;
    width: 100%;
    color: $ColorWhite;
    font-weight: bolder;
    line-height: 69px;

    img.jumbo-image {
        width: 100%;
        height: 100%;
        position: absolute;
    }

    .slider-button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40px;
        height: 40px;
        background-color: rgba(0, 0, 0, 0.5);
        position: absolute;
        top: 50%;
        transform: translate(-50%);
        z-index: 2;
        display: none;
        cursor: pointer;
    }

    .slider-button img {
        width: 15px;
        height: 15px;
        filter: invert(100%);
    }

    .slider-button.prev {
        left: 35px;
    }

    .slider-button.next {
        right: 0;
    }

    div.content {
        z-index: 3;
    }

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

div.jumbotron:hover .slider-button {
    display: flex;
}
</style>