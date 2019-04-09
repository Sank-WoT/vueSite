<template>
  <div id="time">
    <span class="login">Last attack on my site registered in: {{ dateAttack }}</span>
  </div>
</template>

<script>
 import './style.sass'
 import moment from 'moment';
 
 export default {
   name: 'loginTime',
   computed: {
     dateAttack: function() {
       return moment().format('MMMM Do YYYY, h:mm:ss a');
     }
   }
 }
</script>


