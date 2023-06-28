<template>
    <div class="background parallax">
        <div class="container-stats content-container">
            <div class="content d-flex justify-content-between align-items-center">
                <div v-for="stat in dataStatsList" class="stats">
                    <span>{{ stat.number }}</span>
                    <h6>{{ stat.nameStat }}</h6>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataStatsList: [
                {
                    number: 780,
                    nameStat: "SATISFIED CLIENTS",
                },
                {
                    number: 20 + '+',
                    nameStat: "OUR PROJECTS",
                },
                {
                    number: '10,000',
                    nameStat: "CUP OF COFFEE",
                },
                {
                    number: 12,
                    nameStat: "OUR AWARDS",
                },
            ]
        }
    },
}
</script>
<style lang="scss" scoped>
@use "../../styles/utilities/variables.scss" as *;


div.background {
    background-image: url(../../assets/Parallax-01.jpg);

    div.container-stats {
        padding: 98px 0;
        color: $ColorWhite;
        font-weight: bold;

        span {
            font-size: 55px;
        }

        h6 {
            font-size: 17px;
            font-weight: bold;
        }
    }
}
</style>