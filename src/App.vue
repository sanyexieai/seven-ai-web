<script setup lang="ts">
import SideBar from './components/SideBar.vue'
import ChatContent from './components/ChatContent.vue'
</script>

<template>
  <div class="container"> 
    <SideBar />
    <ChatContent message="你好" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 100%;
}
</style>
