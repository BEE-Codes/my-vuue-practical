<template>
  <div>
    hello
    {{add()}}
    <div>

      <button @click="activeD =first">First guy</button>
      <button @click="activeD =second">second guy</button>
      <button @click="activeD = third">third guy</button>

        <component :is="activeD" />
    </div>
  </div>
  
</template>

<script setup lang="ts">
import {ref,shallowRef} from 'vue'


import first from './components/first.vue';
import  second  from './components/second.vue';
import third from './components/third.vue';

const activeD = shallowRef(first);


const abc=ref(null);

function add(){
  return  2 + 2
}

</script>

<style scoped>

</style>