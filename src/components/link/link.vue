<template>
  <span>
    <span><a class="string" :href="href">{{text}}</a></span>
  </span>
</template>

<script>
 import './style.sass'
 export default {
   props: ['href', 'text'],
   name: 'myLink',
 }
</script>
