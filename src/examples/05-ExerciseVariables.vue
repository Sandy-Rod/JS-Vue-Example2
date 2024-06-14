<script>
export default {
  data() {
    return {
      postIt: 'lineas de un post-it',
      arrayString : ['uno', 'dos', 'tres']
    }
  }
}
</script>




<template>
  <div name="divPostit">
      {{ postIt }}
  </div>

  <br>

  <div name="arrayString">
    

      {{ arrayString.join("-") }}
  </div>


</template>

<style scoped>
br {
  color: green;
}
div {
  font-weight: bold;
  color: red;
}
</style>