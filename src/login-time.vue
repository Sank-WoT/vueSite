<template>
  <div id="time">
    <span class="login">Last attack on my site registered in:{{ dateAttack() }}</span>
  </div>
</template>

<script>
 import './style.sass'
 export default {
   name: 'loginTime',
   computed: {
     dateAttack: function() {
       return new Date.now();
     }
   }
 }
</script>


