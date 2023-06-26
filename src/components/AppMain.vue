<template >
    <main>
        <section>
            <Jumbotron />
        </section>
        <section>
            <PeliculaStudio />
        </section>
    </main>
</template>
<script>
import PeliculaStudio from './PeliculaStudio.vue';
import Jumbotron from './Jumbotron.vue';
export default {
    data() {
        return {

        }
    },
    components: {
        PeliculaStudio,
        Jumbotron,
    }
}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;
</style>