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
        <section>
            <TeamMembers />
        </section>
        <section>
            <DescriptionMember />
        </section>
        <section>
            <LatestNews />
        </section>
    </main>
</template>
<script>
import PeliculaStudio from './PeliculaStudio.vue';
import Jumbotron from './Jumbotron.vue';
import AboutUs from './AboutUs.vue';
import WatchList from './WatchList.vue';
import StatsOfProject from './StatsOfProject.vue';
import TeamMembers from './TeamMembers.vue';
import DescriptionMember from './DescriptionMember.vue';
import LatestNews from './LatestNews.vue';
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
        TeamMembers,
        DescriptionMember,
        LatestNews,
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;
</style>