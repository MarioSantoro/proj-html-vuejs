<template>
    <header>
        <a href="#app"><img src="../assets/image (21).svg" alt=""></a>
        <div class="container-nav d-flex justify-content-between align-items-center " id="wrapper">
            <LogoPage />
            <NavBar />
            <SearchAndIcons />
        </div>
    </header>
</template>
<script>
import NavBar from './ComponentsHeader/NavBar.vue';
import SearchAndIcons from './ComponentsHeader/SearchAndIcons.vue';
import LogoPage from './ComponentsHeader/LogoPage.vue';
export default {
    data() {
        return {
        }
    },

    components: {
        NavBar,
        SearchAndIcons,
        LogoPage,
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

header {
    height: 90.98px;
    position: fixed;
    z-index: 5;
    width: 100%;
    box-shadow: 0px -20px 30px 6px #000;
    -moz-box-shadow: 0px -20px 30px 6px #000;
    -webkit-box-shadow: 0px -20px 30px 6px #666;

    div.container-nav {
        padding: 0 40px;
        width: 100%;
        height: 100%;
        background-color: $ColorWhite;
    }

    a {
        position: fixed;
        z-index: 10;
        bottom: 30px;
        right: 30px;
        opacity: 1;
        padding: 9px;
        border: 2px solid $ColorGray;

        img {
            width: 20.39px;
            height: 20.39px;
            filter: invert(50%);
        }
    }
}
</style>