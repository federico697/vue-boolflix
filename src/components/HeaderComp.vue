<template>
  <header class="border border-primary d-flex justify-content-between align-items-center p-3">
    <h1 class="text-danger mb-o">Boolflix</h1>
    <!-- ricerca -->
    <div class="input-group w-50">
      <span class="input-group-text" id="basic-addon1">
        <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
      </span>
      <input type="text"
              class="form-control"
              placeholder="Search..."
              v-model="searchInput"
              @keyup="$emit('emitSearch', searchInput)">
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComp',
  data(){
    return{
      searchInput: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
