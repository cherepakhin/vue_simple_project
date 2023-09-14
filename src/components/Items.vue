<script setup lang="js">
import { ref } from 'vue'

const products = [
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
]

const productsWithRef = ref([
  {id: 10, name: 'shirt10'},
  {id: 20, name: 'jacket20'},
  {id: 30, name: 'shoes30'},
])
</script>

<template>
  <div><h2>Tests:</h2></div>
  <div><h3><u>productsWithRef:</u></h3>
    <!--вывод на экран 0-->
    {{ productsWithRef }}<br/>
  </div>
  <div><h3><u>products:</u></h3>
    <!--вывод на экран 1-->
    {{ products }}
  </div>
</template>
