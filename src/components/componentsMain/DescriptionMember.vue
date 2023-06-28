<template>
    <div class="background parallax">
        <div class="container-member content-container">
            <div class="text-center">
                <img class="wrapper" src="../assets/image (20).svg" alt="Wrapper image">
            </div>
            <div class="content d-flex justify-content-center align-items-center text-center mt-4">
                <div class="member">
                    <div class="text ">
                        <p>{{ dataMemberlist[ActiveIndex].description }}</p>
                        <div class="profile d-flex text-center align-items-center justify-content-center my-4">
                            <div class="image">
                                <img :src="getImagePath(dataMemberlist[ActiveIndex].image)" alt="member image">
                            </div>
                            <div class="name text-start">
                                <h6 class="text-uppercase">{{ dataMemberlist[ActiveIndex].nameMember }}</h6>
                                <p>{{ dataMemberlist[ActiveIndex].role }}</p>
                            </div>
                        </div>
                    </div>
                    <div class="dot">
                        <i v-for="(member, index) in dataMemberlist" class="fa-solid fa-circle" @click="goToImage(index)"
                            :class="ActiveIndex === index ? 'active' : ''"></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataMemberlist: [
                {
                    image: '01.jpg',
                    nameMember: 'John Doe',
                    role: "Designer",
                    description: "Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, idEtiam tempor sit amet metus in bibendum. Nunc eros risus, pellentesque a augue Pellentesque fringilla eget mi eu mollis. Mauris commodo.",
                },
                {
                    image: '02.jpg',
                    nameMember: 'John Doe',
                    role: "Designer",
                    description: "Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, idEtiam tempor sit amet metus in bibendum. Nunc eros risus, pellentesque a augue Pellentesque fringilla eget mi eu mollis. Mauris commodo.",
                },
                {
                    image: '03.jpg',
                    nameMember: 'John Doe',
                    role: "Designer",
                    description: "Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, idEtiam tempor sit amet metus in bibendum. Nunc eros risus, pellentesque a augue Pellentesque fringilla eget mi eu mollis. Mauris commodo.",
                },
            ],
            ActiveIndex: 0,
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../../assets/${img}`, import.meta.url).href;
        },

        goToImage(Index) {
            this.ActiveIndex = Index;
        }
    }
}
</script>
<style lang="scss" scoped>
@use "../../styles/utilities/variables.scss" as *;

div.background {
    background-image: url(../../assets/Parallax-02.jpg);
    background-size: cover;
    background-position: center;

    div.container-member {
        padding: 98px 0;
        color: $ColorWhite;
        font-weight: bold;

        div.image {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;

            img {
                width: 100%;
                height: 100%;
            }
        }

        div.dot i {
            font-size: 10px;
            margin-right: .77rem;
            color: $ColorGray;
        }

        div.dot i.active {
            color: $ColorWhite;
        }

        img.wrapper {
            width: 50px;
            height: 50px;
        }

        div.text {
            width: 790px;

            div.text>p {
                letter-spacing: 0.8px;
            }

            div.name p {
                margin: 0;
                font-size: 14.45px;
            }

        }

        span {
            font-size: 55px;
        }

        h6 {
            font-size: 17px;
            font-weight: bold;
            margin: 0;
        }
    }
}
</style>