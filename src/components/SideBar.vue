<script setup lang="ts">
import { ref } from 'vue'
import Avatar from './Avatar.vue'
</script>

<template>
    <div class="side-bar">
        <div class="side-bar-item" style="flex-direction: row;">
            <svg class="icon" aria-hidden="true">
                <use xlink:href="#icon-shouqi"></use>
            </svg>
            <div class="side-bar-item-row" style="flex: 1;">
                <div style="margin: 0 5px;">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg>    
                </div>
                <div style="flex: 1;font-size: 14px;line-height: 24px; font-weight: bold;">新对话</div>
                <div>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-editor"></use>
                    </svg>  
                </div>
            </div>
        </div>
        <div class="side-bar-item" style="flex: 1; flex-direction: column;">
            <div class="side-bar-title side-bar-item-row ">笔记</div>
            <div class="side-bar-title side-bar-item-row">工作空间</div>
            <div class="side-bar-title side-bar-item-row">搜索</div>
            <div class="side-bar-title side-bar-item-row">对话</div>
        </div>
        <div class="side-bar-item"> 
            <div class="side-bar-item-row">
                <Avatar name="sanye" />
                <div style="margin: 0 10px;flex: 1;font-size: 14px;line-height: 24px; font-weight: bold;">sanye</div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.side-bar {
    width: 260px;
    height: calc(100% - 16px);
    background-color: #f0f0f0;
    display: flex;
    flex-direction: column;
    padding: 8px;
}

.side-bar-item {
    display: flex;
    padding: 4px 8px;
    text-align: left;
}

.side-bar-title {
    font-size: 14px;
    font-weight: bold;
    margin: 5px;
}

.side-bar-item-row {
    display: flex;
    flex-direction: row;
}
.icon {
    width: 24px;
    height: 24px;
}

</style>