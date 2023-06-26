<template>
    <header>
        <div class="container-nav d-flex justify-content-between align-items-center ">
            <div class="logo">
                <img src="../assets/logo.svg" alt="Logo web-site">
            </div>
            <nav>
                <ul class="d-flex align-items-center fw-bold">
                    <li class="text-uppercase h-100" v-for="navItem in listNavBar">
                        <a href="#">{{ navItem }}</a>
                    </li>
                </ul>
            </nav>
            <div class="social d-flex align-items-center justify-content-between">
                <div class="search me-4 ">
                    <img class="svg" src="../assets/image (8).svg" alt="">
                </div>
                <div class="social-icons d-flex align-items-center">
                    <i class="fa-brands fa-facebook-f me-4 svg"></i>
                    <img class="me-4 svg" src="../assets/image (10).svg" alt="">
                    <img class="me-4 svg" src="../assets/image (11).svg" alt="">
                    <img class="svg" src="../assets/image (12).svg" alt="">
                </div>
            </div>
        </div>
    </header>
</template>
<script>
export default {
    data() {
        return {
            listNavBar: [
                "Home",
                "Blog",
                "Pages",
                "About",
                "Contacts",
                "Gallery",
                "Shop",
            ]
        }
    },
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

header {
    height: 90.98px;
    position: fixed;
    width: 100%;
    box-shadow: 0px -20px 30px 6px #000;
    -moz-box-shadow: 0px -20px 30px 6px #000;
    -webkit-box-shadow: 0px -20px 30px 6px #666;

    div.container-nav {
        padding: 0 40px;
        width: 100%;
        height: 100%;
        background-color: $ColorWhite;

        div.logo {
            img {
                width: 187px;
            }

        }

        ul li {
            color: $ColorBlack;
            font-size: 13px;
            margin-right: 2.8rem;

            a {
                text-decoration: none;
                color: $ColorBlack;
            }
        }
    }

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

}
</style>