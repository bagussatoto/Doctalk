<template>
   <nav class="fixed bottom-0 left-0 right-0 bg-white">
      <section class="w-full lg:w-4/12 lg:mx-auto px-5 py-3 flex justify-between ">
         <template v-for="(menu, index) in menus" :key="index">
            <span @click="activeMenu = menu.name" class="duration-300 text-xl" :class="activeMenu === menu.name ? 'text-blue-400' : 'text-gray-300'">
               <i :class="menu.icon"></i>
            </span>
         </template>
      </section>
   </nav>
</template>

<style scoped>
   
   nav {
      box-shadow: -1px 0 14px rgba(0,0,0,.35);
   }
   
</style>

<script setup>
   
   import { ref } from 'vue'
   
   //Menus
   const menus = [
         {
            name: 'bookmark',
            icon: 'fas fa-bookmark'
         },
         {
            name: 'chat',
            icon: 'fas fa-comment'
         },
         {
            name: 'home',
            icon: 'fa fa-home'
         },
         {
            name: 'notification',
            icon: 'fa fa-bell'
         },
         {
            name: 'profile',
            icon: 'fa fa-user'
         }
      ]
      
   //Active menu
   const activeMenu = ref('home')
   
</script>