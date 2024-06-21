<script>
export default {
  data() {
    return {
      dogs: ['Maia', 'Paco', 'Toby'],
      cats: {
        John: 'Fermin',
        Jane: 'Manuela'
      },

      countries: [
        {id:'1' ,name: 'Canada', bandera: 'https://upload.wikimedia.org/wikipedia/commons/d/d9/Flag_of_Canada_%28Pantone%29.svg'},
        {id:'2' ,name: 'Francia', bandera: 'http://enciclopedia.us.es/images/6/6c/Bandera_de_Francia.png'},
        {id:'3' ,name: 'Italia', bandera: 'https://upload.wikimedia.org/wikipedia/commons/0/03/Flag_of_Italy.svg'},
        {id:'4' ,name: 'Portugal', bandera: 'https://upload.wikimedia.org/wikipedia/commons/5/5c/Flag_of_Portugal.svg'},
        {id:'5' ,name: 'Grecia', bandera: 'https://upload.wikimedia.org/wikipedia/commons/5/5c/Flag_of_Greece.svg'}
      ],
      styleFlag: 'flagStyle',
      idRemove: 0


    }
  },
  methods: {
    eliminar(id) {
      console.log(id)
      this.countries.splice(id, 1)
      
    }
  }
}
</script>

<template>
 <!--  

  <ul>
    <li v-for="(dog, index) in dogs" :key="dog">{{ index + 1 }}. {{ dog }}</li>
  </ul>

  ---

  <ul>
    <li v-for="(cat, key, index) in cats" :key="cat">{{ index + 1 }}. {{ key }}: {{ cat }}</li>
  </ul> -->

  <ul>
    <li v-for="(country, key, index) in countries" :key="country"> id: {{ country.id }}, nombre: {{ country.name }} </li>
  </ul>


  <h1> Galeria de imagenes</h1>


  <ul>
    <img v-for="(country, index) in countries" :key="country" :class="styleFlag" :src="country.bandera" :alt="country.name" @click="eliminar(country)" />
  </ul>


</template>



<style>
    .buttonStyle {
    font-size: 15px;
    background-color: rgb(114, 215, 182);
    width: 100px;
    height: 100px;
    padding: 10px;
    margin: 10px;
    border-radius: 10px;
    border: 1px solid black;
  }


  .flagStyle {
    width: 130px;
    height: 130px;
  }
</style>