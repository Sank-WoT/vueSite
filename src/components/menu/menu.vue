<template>
  <div @mouseover="mouseover = true" @mouseleave="mouseover = false">
    <div class="line">
      <span class="comment">/</span>
      <span class="comment">{{head}}</span> 
    </div>

    <div class="line">
      <span class="comment">*</span>
      <span class="white-space space"></span>
      <span v-if="!mouseover"><span class="comment comment_active">{{ menuNameMain[index].trim() }}</span><span class="white-space space"></span></span>
      <span v-else><span v-for="item in menuNameMain"><span class="comment comment_active">{{ item.trim() }}</span><span class="white-space space"></span></span></span><span class="comment">*</span>
    </div>
    <div class="line">
      <span class="comment">{{head}}</span> 
      <span class="comment">/</span>
    </div>
    <div class="line"></div>
  </div>
</template>

<script>
 import './style.sass'
 export default {
   name: 'menu',
   props: ['menuNameMain', 'index'],
   data: function() {
     return {
       mouseover: false,
     }
   },
   computed: {
     head: function() {
       var numberChar = 0;
       this.menuNameMain.forEach(function(el) {numberChar += el.length + 2});
       return '*'.repeat(numberChar - 1);
     }
   },
 }
</script>

