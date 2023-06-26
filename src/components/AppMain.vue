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
        <section>
            <StatsOfProject />
        </section>
    </main>
</template>
<script>
import PeliculaStudio from './PeliculaStudio.vue';
import Jumbotron from './Jumbotron.vue';
import AboutUs from './AboutUs.vue';
import WatchList from './WatchList.vue';
import StatsOfProject from './StatsOfProject.vue';
export default {
    data() {
        return {

        }
    },
    components: {
        PeliculaStudio,
        Jumbotron,
        AboutUs,
        WatchList,
        StatsOfProject,
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;
</style>