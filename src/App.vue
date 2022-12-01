<template>
  <div id="app">
    <HeaderComp @emitSearch="searchFilms" />
    <MainComp :paramFilms="arrayFilms" />
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

// importazione di axios
import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },

  data(){
    return {
      arrayFilms: [],
      serieTv: []
    }
  },

  methods: {
    searchFilms(valoreEmit){
      // chiamata api per i FILM
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=2cdc8fc3444c54094cb66de6879044f4&query=' + valoreEmit)
      .then((res) => {
        this.arrayFilms = res.data.results
      })

      
      // chiamata per serie tv
      // https://api.themoviedb.org/3/search/tv?api_key=e99307154c6dfb0b4750f6603256716d&language=it_IT&query=scrubs
      axios.get('https://api.themoviedb.org/3/search/tv?api_key=2cdc8fc3444c54094cb66de6879044f4&query=' + valoreEmit)
      .then((res) => {
        this.serieTv = res.data.results
      })


    }
  }
}

</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
