<template>
  <span>
    <myConst></myConst><space></space><variable :nameVariable="nameVariable"></variable><space></space><keyword></keyword><string :value="value"></string><semicolon></semicolon>
  </span>
</template>

<script>
 import './style.sass';
 import space from '../space/space.vue';
 import string from '../string/string.vue';
 import variable from '../variable/variable.vue';
 import myConst from '../const/const.vue';
 import semicolon from '../semicolon/semicolon.vue';
 import keyword from '../keyword/keyword.vue';
 export default {
   props: ['value', 'nameVariable'],
   components: {
     space, string, variable, myConst, semicolon, keyword
   },
   name: 'stringLine',
 }
</script>
