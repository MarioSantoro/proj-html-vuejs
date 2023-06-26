<script >
import AppHeader from './components/AppHeader.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    AppHeader,
  }
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@100;200;300;400;500;600;700&display=swap');
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
@import "./styles/general.scss";
</style>
