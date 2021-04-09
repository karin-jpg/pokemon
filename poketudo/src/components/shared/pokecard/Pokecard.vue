<template>
<div id="pokecard">
<div class="card mb-3 flex-row flex-column">
    <p class = "text-center font-weight-bold">{{pokeinfo.forms[0].name}}</p>
    <img :src= "pokeinfo.sprites.front_default" alt="Card image" class="card-img-left">
    <div class="card-body">
        <p class="card-text">
            {{pokedesc.descriptions[2].description}}
        </p>
    </div>
      </div>
  </div>
</template>

<script>

export default {
    props: {
      pokedesc: {
        type: String,
        required: true
      },
      pokeinfo: {
        type: String,
        required: true
      }
    },

    data(){
    }
}

</script>

<style scoped>

</style>