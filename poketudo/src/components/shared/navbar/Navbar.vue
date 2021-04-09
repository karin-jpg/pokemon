<template>
    <div id="app">
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <a class="navbar-brand" href="#">{{titulo}}</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#corNavbar02" aria-controls="corNavbar02" aria-expanded="false" aria-label="Alterna navegação">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="corNavbar02">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#">{{menu1}}</a>
        </li>
      </ul>
    </div>
  </nav>
  </div>
</template>
<script>

export default{
    data() {
        return{
            titulo: 'Poketudo',
            menu1: 'Pokedex'
        }
    }
}
</script>

<style scoped>

</style>