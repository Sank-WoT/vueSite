<template>
  <span>
    <span class="command"></span>
    <span class="args">main.js</span>
  </span>
</template>

<script>
 import './style.sass'
 import TextScramble from './scramble.js'
 export default {
   
   name: 'pathEnd',
   methods: {
     scramble: function() {
       const phrases = [
	 'Loading...',
	 'Cat'
       ]
       const el = document.querySelector('.command');
       const fx = new TextScramble(el);
       let counter = 0;
       let countMax = 1;
       const next = () => {
	 fx.setText(phrases[counter]).then(() => {
	   if(counter != 0) {
	     countMax--;
	     setTimeout(next, 1800);
	   }
	 });
	 counter = (counter + 1) % phrases.length;
       }

       next();
     }
   },

   mounted() {
     this.scramble();
   }
 }
</script>
