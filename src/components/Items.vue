<script setup lang="ts">
import { ref } from 'vue'

const products = [
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
  {id: 2, name: 'shoes'}
]

const productsWithRef = ref([
  {id: 0, name: 'shirt'},
  {id: 1, name: 'jacket'},
  {id: 2, name: 'shoes'}
])

</script>
<template>
  Example cicle (Without 'ref' <i>products = [{id: 0, name: 'shirt'},)]</i>:
  <div 
    v-for='(product, index) in products' 
    :key='product.id' 
  >
    #{{ index + 1}} - {{ product.name }}
  </div>
  Example cicle (WITH 'ref' <i>productsWithRef = ref([{id: 0, name: 'shirt'},...]))</i>:
  <div 
    v-for='(product, index) in productsWithRef' 
    :key='product.id' 
  >
    #{{ index + 1}} - {{ product.name }}
  </div>
</template>
