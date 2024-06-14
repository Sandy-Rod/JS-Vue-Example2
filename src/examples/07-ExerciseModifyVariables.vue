<script>
export default {
  data() {
    return {
      palabra :'',
      palabraAleatoria : '',
      arrayString : ['movil', 'dos', 'silla', 'cuatro', 'taza', 'seis', 'pez', 'ventana', 'sofa'],
      arrayString2 : ['movil2', 'dos2', 'silla2', 'cuatro2', 'taza2', 'seis2', 'pez2', 'ventana2', 'sofa2']
    }
  },
  methods: {
    textoAleatorio() {
      this.palabra = this.arrayString[Math.floor(Math.random() * this.arrayString.length)]
    },

    mouseOver(){
      this.palabraAleatoria = this.arrayString2[Math.floor(Math.random() * this.arrayString2.length)]
    }
  }
}
</script>

<template>
  <div class="flex flex-col gap-5 w-full items-center">
    <button
      class="w-32 border-2 rounded-lg bg-gray-100 hover:bg-blue-100 border-blue-400"
      @click="textoAleatorio"
    > texto aleatorio
      
    </button>
    <p>{{ palabra }}</p>

    <button
      class="w-32 border-2 rounded-lg bg-gray-100 hover:bg-blue-100 border-blue-400"
      @mouseover="mouseOver"
    >
      otro texto aleatorio 2
    </button>
    <p>{{ palabraAleatoria }}</p>

  </div>
</template>
