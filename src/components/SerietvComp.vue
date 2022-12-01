<template>
    <div class="row gx-4 gy-4">
        <SerieCard v-for="(elem, index) in SerieTv" :key="index" :singolaSerie="elem"/>
    </div>
</template>

<script>
import  SerieCard from './SerieCard.vue'

    export default {
        name: 'SerietvComp',
        components:{
            SerieCard
        },
        props:{
            SerieTv: Array
        }
    }
</script>

<style lang="scss" scoped>

</style>