<template>
  <div>
    <div class="line">
      <loginTime></loginTime>      
    </div>

    <div class="line" style="font-size: 0;">
      <pathLine testString="~/sank"></pathLine>
      <pathAdd testString="master"></pathAdd>
      <pathEnd></pathEnd>
    </div>
    <div class="line"></div>
    <menuMain v-bind:menuNameMain="['Profile', 'Skills', 'Projects']"></menuMain>
    <div class="line">
      <stringLine nameVariable="myName" value="Aleksandr Serobabov"></stringLine>
    </div>
    <div class="line">
      <stringLine nameVariable="profession" value="I speak Code"></stringLine>
    </div>
    <div class="line">
      <stringLine nameVariable="email" value="aserobabow95@mail.ru"></stringLine> 
    </div>

    <div class="line"></div>
    
    <div class="line">
      <linkLine nameVariable="github" href="https://github.com/Sank-WoT" text="https://github.com/Sank-WoT"></linkLine>
    </div>
    <div class="line">
      <linkLine nameVariable="vk" href="https://vk.com/sank_revenge" text="https://vk.com/sank_revenge"></linkLine>
    </div>

    <div class="line"></div>
    <div class="skillset collapsed">
      <div class="line">
	<list title="Frontend"></list>
      </div>      
    </div>
  </div>
</template>

<script>
 import loginTime from './components/login/login-time.vue';
 import pathLine from './components/path/path.vue';
 import pathAdd from './components/pathAdd/path.vue';
 import menuMain from './components/menu/menu.vue';
 import pathEnd from './components/pathEnd/path.vue';
 import space from './components/space/space.vue';
 import stringLine from './components/stringLine/stringLine.vue'
 import linkLine from './components/linkLine/linkLine.vue';
 import list from './components/list/list.vue';
 import './style.sass'
 export default {
   components: {
     loginTime, pathLine, pathAdd, menuMain, pathEnd, space, stringLine, linkLine, list
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
