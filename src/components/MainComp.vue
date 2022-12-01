<template>
    <main class="">
        <h2>main</h2>
        <!-- sezione films e serietv-->
        <div class="container">
            <h2 class="my-5 text-center" >Films</h2>
            <FilmsComp :filmsData="paramFilms"/>
            <h2 class="my-5 text-center" >Serie TV</h2>
            <SerietvComp :SerieTv="paramSerieTv"/>
        </div>
    </main>
</template>

<script>
import FilmsComp from './FilmsComp.vue';
import SerietvComp from './SerietvComp.vue'

    export default {
        name: 'MainComp',
        props:{
            paramFilms: Array,
            paramSerieTv: Array
        },
        components:{
            FilmsComp,
            SerietvComp
        }
    }
</script>

<style lang="scss" scoped>

</style>