<script setup lang="ts">
import { ref } from 'vue'
import Avatar from './Avatar.vue'
</script>

<template>
    <div class="side-bar">
        <div class="side-bar-item side-bar-item-row side-bar-item-row-top">
            <svg class="icon" aria-hidden="true">
                <use xlink:href="#icon-shouqi"></use>
            </svg>
            <div class="side-bar-item-row side-bar-item-row-main">
                <div class="side-bar-item-icon">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-seven"></use>
                    </svg>    
                </div>
                <div class="side-bar-item-title">新对话</div>
                <div>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-editor"></use>
                    </svg>  
                </div>
            </div>
        </div>
        <div class="side-bar-item side-bar-item-col side-bar-item-flex">
            <div class="side-bar-title side-bar-item-row">笔记</div>
            <div class="side-bar-title side-bar-item-row">工作空间</div>
            <div class="side-bar-title side-bar-item-row">搜索</div>
            <div class="side-bar-title side-bar-item-row">对话</div>
        </div>
        <div class="side-bar-item"> 
            <div class="side-bar-item-row">
                <Avatar name="sanye" />
                <div class="side-bar-user">sanye</div>
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

.side-bar-item-row {
    display: flex;
    flex-direction: row;
}

.side-bar-item-row-top {
    flex-direction: row;
}

.side-bar-item-row-main {
    flex: 1;
    align-items: center;
}

.side-bar-item-icon {
    margin: 0 5px;
}

.side-bar-item-title {
    flex: 1;
    font-size: 14px;
    line-height: 24px;
    font-weight: bold;
}

.side-bar-item-col {
    flex-direction: column;
}

.side-bar-item-flex {
    flex: 1;
}

.side-bar-title {
    font-size: 14px;
    font-weight: bold;
    margin: 5px;
}

.side-bar-user {
    margin: 0 10px;
    flex: 1;
    font-size: 14px;
    line-height: 32px;
    font-weight: bold;
}

.icon {
    width: 24px;
    height: 24px;
}
</style>