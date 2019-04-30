<template>
  <span>
    <span class="comment">//<space></space>{{title}}</span>
  </span>
</template>

<script>
 import './style.sass'
 import space from '../space/space.vue';
 import collapsed from '../collapsed/collapsed.vue';
 export default {
   props: ['title'],
   name: 'elementParentList',
   components: {
     space, collapsed
   }
 }
</script>
