<template>
  <div class="flex  min-h-full">
    <!-- Sidebar -->
    <Sidebar :class="{'-ml-[200px]': !sidebarOpened}"/>
    <!-- Main -->
    <div class="flex-1">
      <Navbar @toggle-sidebar="toggleSidebar"/>
      <!-- <header class="h-8 shadow bg-white">
        Header
      </header> -->
      <main class="p-6">
        <div class="p-4 rounded bg-white">
          <router-view></router-view>
        </div>
      </main>
    </div>
  
  </div>
</template>

<script setup>
import {ref, onMounted, onUnmounted} from 'vue'
import Sidebar from "./Sidebar.vue";
import Navbar from "./Navbar.vue";

const { title } = defineProps({
  title: String
})

const sidebarOpened = ref(true);

function toggleSidebar() {
  sidebarOpened.value = !sidebarOpened.value
}

function updateSidebarState() {
  sidebarOpened.value = window.outerWidth > 768;
}

onMounted(() => {
  
  updateSidebarState();
  window.addEventListener('resize', updateSidebarState)
})

onUnmounted(() => {
  window.removeEventListener('resize', updateSidebarState)
})

</script>

<style scoped></style>