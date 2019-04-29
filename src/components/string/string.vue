<template>
  <span>
    <span v-for="item in text" class="string"><space></space>{{item}}</span>
  </span>
</template>

<script>
 import './style.sass'
 import space from '../space/space.vue';
 export default {
   components: {
     space
   },
   name: 'myString',
   props: ['value'],
   computed: {
     text: function() {
       return this.value.split(' ');
     }
   },
 }
</script>
