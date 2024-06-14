<script>
export default {
  data() {
    return {
      myId: 'test-id',
      titleClass: 'title',
      styleButton : 'buttonStyle',
      isActive: true,
      hasError: true,
      errorClass: 'error',
      fontSize: '30px',
      color: 'green',
      colorTexto : 'black',
      colorPostit : 'black',
      colorList: ['red', 'green', 'gold', 'pink']
    }
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive
    },

    textoColor(color) { 
      this.colorTexto = color
    },

    mouseOver(){
      this.colorPostit = this.colorList[Math.floor(Math.random() * this.colorList.length)]
    },

    created() { 
    console.log(`Component created by ${this.name}`)
  },
    mounted() {
    console.log(`Component mounted by ${this.name}`)
  }


  }
}
</script>

<template>
  
<!--
  <div class="flex flex-col gap-5">
    <div v-bind:id="myId">This div has a dynamic id: {{ myId }}, inspect it!</div>
    <h1 :class="titleClass">This is a title with a dynamic class</h1>
    <p :class="{ 'active-title': isActive }" @click="toggleActive">
      This is a text that changes the color if it's active. Click it to toggle it!
    </p>
    <h1 :class="[hasError ? errorClass : '', titleClass]">This is a title with an error state</h1>
    <h1 :style="{ color: color, fontSize: fontSize }">
      This is a title using inline dynamic styles
    </h1>
  </div>
-->
  <div class="divColores">
    <button @click="textoColor(colorList[0])" :class="styleButton" :style="{backgroundColor:colorList[0]}">{{ colorList[0] }}</button>
    <button @click="textoColor(colorList[1])" :class="styleButton" :style="{backgroundColor:colorList[1]}">{{ colorList[1] }}</button>
    <button @click="textoColor(colorList[2])" :class="styleButton" :style="{backgroundColor:colorList[2]}">{{ colorList[2] }}</button>
    <button @click="textoColor(colorList[3])" :class="styleButton" :style="{backgroundColor:colorList[3]}">{{ colorList[3] }}</button>
  </div>
  <br>
  <p :style="{color:colorTexto}"> TEXTO COLORES ALEATORIOS </p>
  <br>
  <br>
  <br>

  <div class="post-it"  @mouseover="mouseOver" :style="{ color: colorPostit }">
    <h3>Recordatorio</h3>
    <p>No olvides enviar el informe.</p>
  </div>

</template>

<style>
.title {
  font-size: 22px;
}
.active-title {
  color: green;
}

.error {
  color: red;
}

.buttonStyle {
  font-size: 15px;
  width: 100px;
  height: 100px;
  padding: 10px;
  margin: 10px;
  border-radius: 10px;
  border: 1px solid black;
}

.post-it {
  width: 200px;
  height: 200px;
  padding: 15px;
  background-color: #fffa77;
  border: 1px solid #d4d4d4;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.1);
  position: relative;
  transform: rotate(-3deg);
  text-align: center;
  font-size: 16px;
}

</style>




