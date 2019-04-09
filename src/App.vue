<template>
  <div>
    <div class="line">
      <loginTime></loginTime>      
    </div>

    <div class="line" style="font-size: 0;">
      <pathLine testString="~/sank"></pathLine>
      <pathAdd testString="master"></pathAdd>
    </div>
  </div>
</template>

<script>
 import loginTime from './components/login/login-time.vue';
 import pathLine from './components/path/path.vue';
 import pathAdd from './components/pathAdd/path.vue';
 export default {
   components: {
     loginTime, pathLine, pathAdd
   },
   name: 'app',
   data () {
     return {
       msg: 'root'
     }
   }
 }
</script>
</style>
