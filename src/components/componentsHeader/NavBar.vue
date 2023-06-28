<template>
    <nav class="h-100 ">
        <ul class="d-flex fw-bold h-100">
            <li class="text-uppercase h-100 d-flex align-items-center" v-for="navItem in listNavBar">
                <a v-if="navItem == 'Pages' || navItem == 'Shop'" href="#">{{ navItem }} <i
                        class="fa-solid fa-chevron-down fa-xs"></i></a>
                <a v-else href="#">{{ navItem }}</a>
                <div v-if="navItem == 'Pages'" class="drop-menu">
                    <ul class="text-uppercase">
                        <li class="bord li-drop-menu">
                            Services
                        </li>
                        <li class="bord li-drop-menu">
                            our work flow
                        </li>
                        <li class="li-drop-menu">
                            Video Thumbnail type
                        </li>
                    </ul>
                </div>

                <div v-if="navItem == 'Shop'" class="drop-menu shop">
                    <ul class="text-uppercase">
                        <li class="bord d-flex justify-content-between align-items-center li-drop-menu">
                            Shop Pages
                            <img src="../../assets/right-arrow.svg" alt="">
                            <div class="shop-menu">
                                <ul class="text-uppercase">
                                    <li class="bord li-drop-menu">My account</li>
                                    <li class="bord li-drop-menu">Checkout</li>
                                    <li class="li-drop-menu">Cart</li>
                                </ul>
                            </div>
                        </li>
                        <li class=" d-flex justify-content-between align-items-center li-drop-menu">
                            product type
                            <img src="../../assets/right-arrow.svg" alt="">
                            <div class="shop-menu second">
                                <ul class="text-uppercase">
                                    <li class="bord li-drop-menu">External/Affiliate product</li>
                                    <li class="bord li-drop-menu">Group Product</li>
                                    <li class="bord li-drop-menu">Simple Product</li>
                                    <li class="li-drop-menu">Variable Product</li>
                                </ul>
                            </div>
                        </li>
                    </ul>
                </div>
            </li>
        </ul>
    </nav>
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
<style lang="scss">
@use "../../styles/utilities/variables.scss" as *;

nav ul li {
    font-size: 13px;
    margin-right: 2.8rem;

    a {
        text-decoration: none;
        color: $ColorBlack;
    }

    div.drop-menu,
    .shop-menu {
        display: none;

    }

    div.drop-menu {
        position: absolute;
        bottom: -145px;

        ul li.bord {
            border-bottom: 1px solid $ColorGray;
        }

        ul li:hover {
            color: $ColorGray;
        }
    }

    div.drop-menu.shop {
        bottom: -96px;

        img {
            width: 10px;
            height: 10px;
            filter: invert(100%);
        }

        div.shop-menu {
            position: absolute;
            right: -300px;
            bottom: -48.7px;
        }

        div.shop-menu.second {
            bottom: -145px;
        }

        ul li:hover div.shop-menu {
            display: block;
        }
    }

}

ul li:hover div.drop-menu {
    display: block;
}

.li-drop-menu {
    color: $ColorWhite;
    background-color: $ColorBlack;
    padding: .88rem .66rem;
    width: 300px;
    cursor: pointer;
    transition: all .2s ease;
}
</style>