<template >
    <main>
        <section>
            <Jumbotron />
        </section>
        <section>
            <PeliculaStudio />
        </section>
        <section>
            <AboutUs />
        </section>
        <section>
            <WatchList />
        </section>
    </main>
</template>
<script>
import PeliculaStudio from './PeliculaStudio.vue';
import Jumbotron from './Jumbotron.vue';
import AboutUs from './AboutUs.vue';
import WatchList from './WatchList.vue';
export default {
    data() {
        return {

        }
    },
    components: {
        PeliculaStudio,
        Jumbotron,
        AboutUs,
        WatchList
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;
</style>