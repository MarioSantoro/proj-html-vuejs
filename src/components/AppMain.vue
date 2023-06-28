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
        <section class="position-relative">
            <LatestNews />
        </section>
        <section>
            <Icons />
        </section>
        <section>
            <Appform />
        </section>
    </main>
</template>
<script>
import PeliculaStudio from './componentsMain/PeliculaStudio.vue';
import Jumbotron from './componentsMain/Jumbotron.vue';
import AboutUs from './componentsMain/AboutUs.vue';
import WatchList from './componentsMain/WatchList.vue';
import StatsOfProject from './componentsMain/StatsOfProject.vue';
import TeamMembers from './componentsMain/TeamMembers.vue';
import DescriptionMember from './componentsMain/DescriptionMember.vue';
import LatestNews from './componentsMain/LatestNews.vue';
import Icons from './componentsMain/Icons.vue';
import Appform from './componentsMain/Appform.vue';
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
        Icons,
        Appform,
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;
</style>