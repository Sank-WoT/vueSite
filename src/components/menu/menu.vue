<template>
  <div>
    <div class="line">
      <span class="comment">/</span>
      <span class="comment">{{head}}</span> 
    </div>

    <div class="line">
      <span class="comment">*</span>
      <span class="white-space space"></span>
      <span class="comment comment_active">{{menuNameMain[0]}}</span>
      <span v-for="item in menuNameMain">
	<span class="comment comment_active">{{ item.trim() }}</span>
	<span class="white-space space"></span>
      </span>
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
   props: ['menuNameMain'],
   computed: {
     head: function() {
       var numberChar = 0;
       this.menuNameMain.forEach(function(el) {numberChar += el.length + 1});
       console.log(numberChar);
       return '*'.repeat(numberChar);
     }
   }
 }
</script>

