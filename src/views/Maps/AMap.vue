<template>
  <div id="container"></div>
</template>

<script setup>
import { ref } from 'vue'
const map = ref({})

// init AMap

AMapLoader.load({
  key: 'e2451f84296a948ed38d7e730f066c23',
  version: '2.0'
})
  .then((AMap) => {
    map.value = new AMap.Map('container', {
      zoom: 10,
      center: [116.397428, 39.90923]
    })
  })
  .catch((e) => {
    console.error(e)
  })
</script>

<style scoped>
#container {
  width: 100%;
  height: 100vh;
}
</style>
