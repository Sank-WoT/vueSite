<template>
  <span v-on:click="expend">
    <div class="line"><elementParentList :title="title"></elementParentList></div>
    <listLevel :title="title" textLevel2="wordpress"></listLevel>
  </span>
</template>

<script>
 import './style.sass'
 import space from '../space/space.vue';
 import collapsed from '../collapsed/collapsed.vue';
 import elementParentList from '../elementParentList/elementParentList.vue';
 import listLevel from '../listLevel/listLevel.vue';
 export default {
   data: function() {
     return {expended: true};
   },
   props: ['title'],
   components: {
     space, collapsed, elementParentList, listLevel
   },
   methods: {
     expend: function() {
       this.expended = !this.expended
       return this.expended;
     }
   },
   name: 'list',
 }
</script>
