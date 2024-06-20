<!-- Crear un visor de imagenes, que dependiendo del pais que seleccione el usuario (pueden ser
botones los paises), muestre una imagen u otra, usando condicionales en los templates.
 -->
<script>
  export default {
    data() {
  return {
        active: true,
        Pais: '',
        src: '',
        styleButton : 'buttonStyle',
        styleFlag: 'flagStyle',
        type: 'car',

        countries: [
          {name: 'Canada', bandera: 'https://upload.wikimedia.org/wikipedia/commons/d/d9/Flag_of_Canada_%28Pantone%29.svg'},
          {name: 'Francia', bandera: 'http://enciclopedia.us.es/images/6/6c/Bandera_de_Francia.png'},
          {name: 'Italia', bandera: 'https://upload.wikimedia.org/wikipedia/commons/0/03/Flag_of_Italy.svg'}
        ]
      } 
    },
    methods: {
      toggleActive() {
        this.active = !this.active
      }, 

    mostrarBandera(paisSeleccionado){
        this.Pais = paisSeleccionado
        this.src = this.countries.find(p => p.name == paisSeleccionado).bandera
        
      } 
    }
  }

</script>

<template>
  <!--
  <button
    @click="toggleActive"
    class="w-32 border-2 rounded-lg bg-gray-100 hover:bg-blue-100 border-blue-400"
  >
    Toggle active
  </button>
  <h1 v-if="active">v-if: This will be shown if active is true</h1>
  <h1 v-show="!active">v-show: This will be shown if active is false</h1>
  <br />
  <div v-if="type === 'car'">This is a car</div>
  <div v-else-if="type === 'moto'">This is a moto</div>
  <div v-else>This is a horse</div>
  <br /> -->


  <div>
    <button @click="mostrarBandera(countries[0].name )" :class="styleButton" > {{ countries[0].name }} </button>
    <button @click="mostrarBandera(countries[1].name )" :class="styleButton" > {{ countries[1].name }} </button>
    <button @click="mostrarBandera(countries[2].name )" :class="styleButton" > {{ countries[2].name }} </button>
  </div>


   <div :class="styleFlag" v-if="Pais === countries[0].name"> <img :src="src"/> </div> 

    <div :class="styleFlag" v-else-if="Pais === countries[1].name"> <img :src="src"/> </div>

    <div :class="styleFlag" v-else > <img :src="src"/>  </div> 


</template> 




<style>
  .buttonStyle {
    font-size: 15px;
    background-color: aquamarine;
    width: 100px;
    height: 100px;
    padding: 10px;
    margin: 10px;
    border-radius: 10px;
    border: 1px solid black;
  }


  .flagStyle {
    width: 200px;
    height: 200px;
  }
</style>
