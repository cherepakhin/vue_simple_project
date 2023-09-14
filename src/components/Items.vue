<script setup lang="js">
import { ref } from 'vue'

const products = [
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
]

const productsWithRef = ref([
  {id: 0, name: 'shirt0'},
  {id: 1, name: 'jacket1'},
  {id: 3, name: 'shoes3'}
])

</script>

<template>
  <div><u>Example cicle</u> (Without 'ref' <i>products = [{id: 0, name: 'shirt'},)]</i>:</div>
  <div class="greetings"
    v-for='(product, index) in products' 
    :key='product.id' 
  >
    #index:{{ index + 1}}  id:{{product.id }}  name:{{ product.name }}
  </div>
  <u>Example cicle</u> (WITH 'ref' <i>productsWithRef = ref([{id: 0, name: 'shirt'},...]))</i>:
  <div 
    v-for='(product, index) in productsWithRef' 
    :key='product.id' 
  >
    #index:{{ index + 1}}  id:{{product.id }}  name:{{ product.name }}
  </div>
  <!-- reverse ниже влияет на отображение выше в div v-for-->
  <div><u>productsWithRef.reverse() 1 раз</u>:<br/> {{ productsWithRef.reverse() }}</div>
  <!--[ { "id": 3, "name": "shoes3" }, { "id": 1, "name": "jacket" }, { "id": 0, "name": "shirt" } ]-->
  <div><u>productsWithRef.reverse() 2 раз</u>:<br/>{{ productsWithRef.reverse() }}</div>
  <!--[ { "id": 0, "name": "shirt" }, { "id": 1, "name": "jacket" }, { "id": 3, "name": "shoes3" } ]-->
  <div><u>products.reverse()</u>:<br/> {{ products.reverse() }}</div>
</template>
