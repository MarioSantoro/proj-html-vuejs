<template>
    <header>
        <div class="container-nav d-flex justify-content-between align-items-center ">
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
    z-index: 3;
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
}
</style>