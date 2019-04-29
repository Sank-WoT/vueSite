<template>
  <span class="variable">{{nameVariable}}</span>
</template>

<script>
 import './style.sass'
 
 export default {
   name: 'myConst',
   props: ['nameVariable']
 }
</script>
