<template>
    <main class="">
        <!-- sezione films -->
        <h2>main</h2>
        <div class="container">
            <FilmsComp :filmsData="paramFilms"/>
        </div>
    </main>
</template>

<script>
import FilmsComp from './FilmsComp.vue'

    export default {
        name: 'MainComp',
        props:{
            paramFilms: Array
        },
        components:{
            FilmsComp
        }
    }
</script>

<style lang="scss" scoped>

</style>