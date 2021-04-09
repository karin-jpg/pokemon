<template>
<div>
  <navbar></navbar>
  <div id ="menu-pokecard" class="d-flex justify-content-center align-items-center flex-column">
    <div id="div-pokecard" >
      <pokecard :pokedesc = "this.pokemonDesc" :pokeinfo = "this.pokemonInfo"></pokecard>
    </div>
    <div id="teste">
      <botaoMenu></botaoMenu>
    </div>
  </div>
</div>
</template>

<script>

import Navbar from './../navbar/Navbar.vue'
import Pokecard from './../pokecard/Pokecard.vue'
import BotaoMenu from './../botao-menu/BotaoMenu.vue'



export default{

  components: {
    'navbar': Navbar,
    'pokecard':Pokecard,
    'botaoMenu':BotaoMenu
  },

    data(){

    return{
      pokemonInfo: [],
      pokemonDesc: [],
      nome: 'alo'
    }
  },

  created() {
    let promiseDesc= this.$http.get('https://pokeapi.co/api/v2/characteristic/1');
    promiseDesc
    .then(res => res.json())
    .then(pokemon => this.pokemonDesc = pokemon, err => console.log(err))

    let promiseInfo= this.$http.get('http://pokeapi.co/api/v2/pokemon/1');
    promiseInfo
    .then(res => res.json())
    .then(pokemon => this.pokemonInfo = pokemon, err => console.log(err))
    
  }
}
</script>

<style lang="scss">
#menu-pokecard {
  width: 100%;
  height: 50vh;
  float:right;
}
</style>
