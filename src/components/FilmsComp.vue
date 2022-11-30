<template>
    <div class="row gx-4 gy-4">
        <FilmCard v-for="(elem, index) in filmsData"
         :key="index" :singleFilm="elem"/>
    </div>
</template>

<script>
import FilmCard from './FilmCard.vue'

    export default {
        name: 'FilmsComp',
        components:{
            FilmCard
        },
        props: {
            filmsData: Array
        }
    }
</script>

<style lang="scss" scoped>

</style>