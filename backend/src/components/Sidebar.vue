<template>
  <div class="min-w-[160px] w-[200px]  transition-all bg-indigo-700 text-white py-4 px-2">
    <router-link :to="{name: 'app.dashboard'}"
                 class="flex items-center p-3 rounded transition-colors hover:bg-black/30">
      <span class="mr-2 text-gray-300">
        <HomeIcon class="w-5"/>
      </span>
      <span class="text-xs">
        Dashboard
      </span>
    </router-link>
    <router-link :to="{name: 'app.products'}"
                 class="flex items-center p-3 rounded transition-colors hover:bg-black/30">
      <span class="mr-2 text-gray-300">
        <ShoppingBagIcon class="w-5"/>
      </span>
      <span class="text-xs">
        Продукты
      </span>
    </router-link>
    <router-link :to="{name: 'app.dashboard'}"
                 class="flex items-center p-3 rounded transition-colors hover:bg-black/30">
      <span class="mr-2 text-gray-300">
        <UsersIcon class="w-5"/>
      </span>
      <span class="text-xs">
        Пользователи
      </span>
    </router-link>
    
  </div>
</template>

<script setup>
  import {HomeIcon, UserGroupIcon, UsersIcon, ChartBarIcon, ShoppingBagIcon} from '@heroicons/vue/24/outline'
</script>

<style scoped>

</style>