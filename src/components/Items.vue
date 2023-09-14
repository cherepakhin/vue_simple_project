<script setup lang="js">
import { ref } from 'vue'

const products = [
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
]

const productsWithRef = ref([
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
  {id: 3, name: 'shoes3'}
])

</script>
<template>
  Example cicle (Without 'ref' <i>products = [{id: 0, name: 'shirt'},)]</i>:
  <div 
    v-for='(product, index) in products' 
    :key='product.id' 
  >
    #index:{{ index + 1}}  id:{{product.id }}  name:{{ product.name }}
  </div>
  Example cicle (WITH 'ref' <i>productsWithRef = ref([{id: 0, name: 'shirt'},...]))</i>:
  <div 
    v-for='(product, index) in productsWithRef' 
    :key='product.id' 
  >
    #index:{{ index + 1}}  id:{{product.id }}  name:{{ product.name }}
  </div>
  <div>{{ productsWithRef.reverse() }}</div>
  <div>{{ productsWithRef.reverse() }}</div>
  <!-- <div>{{ productsWithRef.reverse() }}</div> -->
</template>
