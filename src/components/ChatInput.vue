<script setup lang="ts">
import { ref, computed} from 'vue'

</script>

<template>
    <div class="chat-input">
        <div class="chat-input-box">
            <input type="text" placeholder="有什么我能帮你的吗" />
        </div>
        <div class="chat-input-tools">
            <div class="chat-input-tools-item">
                <div class="tool-button">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg> 
                </div>
                <div class="tool-button">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg> 
                    <span>联网搜索</span>
                </div>
                <div class="tool-button">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg> 
                    <span>代码解释器</span>
                </div>
            </div>
            <div class="chat-input-tools-item">
                <div class="tool-button">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg> 
                </div>
                <div class="tool-button">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg> 
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.chat-input {
    width: 100%;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.chat-input-box {
    padding: 12px 16px;
    border-bottom: 1px solid #f0f0f0;
}

.chat-input-box input {
    width: 100%;
    height: 40px;
    padding: 0 16px;
    border: 1px solid #e8e8e8;
    border-radius: 6px;
    font-size: 14px;
    transition: all 0.3s;
    outline: none;
}

.chat-input-box input:focus {
    border-color: #1890ff;
    box-shadow: 0 0 0 2px rgba(24, 144, 255, 0.1);
}

.chat-input-box input::placeholder {
    color: #999;
}

.chat-input-tools {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 8px 16px;
    background: #fafafa;
    border-radius: 0 0 8px 8px;
}

.chat-input-tools-item {
    display: flex;
    flex-direction: row;
    gap: 8px;
}

.tool-button {
    display: flex;
    align-items: center;
    gap: 4px;
    padding: 6px 12px;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.2s;
    color: #666;
    font-size: 13px;
}

.tool-button:hover {
    background: #f0f0f0;
    color: #1890ff;
}

.tool-button .icon {
    width: 16px;
    height: 16px;
}
</style>