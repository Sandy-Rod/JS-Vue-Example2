<script>
export default {
  data() {
    return {
      styleButton : 'buttonStyle',
      styleFlag: 'flagStyle',


      countries: [
        {id:'1' ,name: 'Canada', bandera: 'https://upload.wikimedia.org/wikipedia/commons/d/d9/Flag_of_Canada_%28Pantone%29.svg'},
        {id:'2' ,name: 'Francia', bandera: 'http://enciclopedia.us.es/images/6/6c/Bandera_de_Francia.png'},
        {id:'3' ,name: 'Italia', bandera: 'https://upload.wikimedia.org/wikipedia/commons/0/03/Flag_of_Italy.svg'},
        {id:'4' ,name: 'Portugal', bandera: 'https://upload.wikimedia.org/wikipedia/commons/5/5c/Flag_of_Portugal.svg'},
        {id:'5' ,name: 'Grecia', bandera: 'https://upload.wikimedia.org/wikipedia/commons/5/5c/Flag_of_Greece.svg'}
      ]


    }
  }
}
</script>

<template>
  <p>This is a sandbox, start creating your exercise!</p>
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