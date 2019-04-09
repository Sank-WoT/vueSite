<template>
  <span class="pathAdd"><i class="fas fa-code-branch"></i> {{testString}}</span>
</template>

<script>
 import './style.sass'
 
 export default {
   name: 'pathAdd',
   props: ['testString']
 }
</script>
