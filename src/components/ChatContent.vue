<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
    <div class="chat-content">
        <div class="chat-content-header">
            <div class="chat-content-header-avatar">

            </div>
            <div class="chat-content-header-name">
                <span>张三</span>
                <span>在线</span>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .chat-content {
        flex: 1;
        background-color: #fff;
    }
    
    
</style>
