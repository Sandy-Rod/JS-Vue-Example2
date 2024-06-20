<!-- Crear un texto que cuando hagas click en el, se convierta en un input de texto, como si
estuviera en modo edición -->

<script>
export default {
  data() {
    return {
      active: false,
      text: "texto inactivo"
    }
  },
  methods: {
    activeInput() {
      this.active =!this.active
    }

  }
}
</script>

<template>
  <p @click="activeInput" v-if="!active" >{{ text }}</p>
  <input v-show="active" :value="text"> 
</template>





<style>

</style>