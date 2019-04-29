<template>
  <span>
    <myConst></myConst><space></space><variable :nameVariable="nameVariable"></variable><space></space><keyword></keyword><link :href="href" :text="text"></string><semicolon></semicolon>
  </span>
</template>

<script>
 import './style.sass';
 import space from '../space/space.vue';
 import link from '../link/link.vue';
 import variable from '../variable/variable.vue';
 import myConst from '../const/const.vue';
 import semicolon from '../semicolon/semicolon.vue';
 import keyword from '../keyword/keyword.vue';
 export default {
   props: ['nameVariable', 'href', 'text'],
   components: {
     space, link, variable, myConst, semicolon, keyword
   },
   name: 'linkLine',
 }
</script>
