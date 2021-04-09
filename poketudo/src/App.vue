<template>
<div>
  <meu-menu></meu-menu>
</div>
</template>

<script>

import Vue from 'vue'
import BootstrapVue from "bootstrap-vue"
import Menu from "./components/shared/home/Home.vue"
import "./../node_modules/bootstrap/dist/css/bootstrap.min.css"
import "./../node_modules/bootstrap-vue/dist/bootstrap-vue.css"


Vue.use(BootstrapVue)

export default{

  components: {
    'meu-menu': Menu
  }
}

</script>

<style lang="scss">
</style>
