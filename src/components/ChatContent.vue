<script setup lang="ts">
import { ref } from 'vue'
import Avatar from './Avatar.vue'
import ChatInput from './ChatInput.vue'
import ChatTip from './ChatTip.vue'
import ChatMessage from './ChatMessage.vue'
const props = defineProps<{ message: string }>()
</script>

<template>
    <div class="chat-content">
        <div class="chat-content-header">
            <div class="chat-content-header-model">
                <div class="model-info">
                    <div class="model-name">llama3.2:latest</div>
                    <div class="model-icon">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-xiangxia"></use>
                        </svg>  
                    </div>
                    <div class="model-icon">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-tianjia"></use>
                        </svg>  
                    </div>
                </div>
                <div class="model-default">
                    <div>设为默认</div>
                </div>
            </div>
            <div class="chat-content-header-avatar">
                <div class="spacer"></div>
                <div class="avatar-group">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-gaojishezhi"></use>
                    </svg>  
                    <Avatar name="sanye" />
                </div>
            </div>
        </div>
        <div v-if="props.message" class="chat-content-body">
            <div class="chat-content-body-message">
                <ChatMessage />
            </div>
            <div class="chat-content-body-input">
                <ChatInput />
            </div>
        </div>

        <div v-else class="chat-content-body chat-content-body-empty">
            <div class="chat-content-body-title">
                <div class="title-icon">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-seven"></use>
                    </svg>    
                </div>
                <div class="title-text">llama3.2:latest</div>
            </div>
            <div class="chat-content-body-input">
                <ChatInput />
            </div>
            <div class="chat-content-body-tip">
                <ChatTip />
            </div>
        </div>
    </div>
</template>

<style scoped>
    .chat-content {
        flex: 1;
        display: flex;
        flex-direction: column;
        background-color: #fff;
        box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
        margin: 16px;
        overflow: hidden;
    }

    .chat-content-header {
        height: 60px;
        display: flex;
        flex-direction: row;
        padding: 0 20px;
        border-bottom: 1px solid #f0f0f0;
        background-color: #fafafa;
        align-items: center;
    }

    .chat-content-header-model {
        flex: 1;
        display: flex;
        flex-direction: column;
        gap: 4px;
    }

    .model-info {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 8px;
    }

    .model-name {
        font-weight: 500;
        color: #333;
    }

    .model-icon {
        display: flex;
        align-items: center;
    }

    .model-default {
        font-size: 13px;
        color: #666;
        cursor: pointer;
        transition: color 0.2s;
        text-align: left;
    }

    .model-default:hover {
        color: #1890ff;
    }

    .chat-content-header-avatar {
        flex: 1;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        gap: 12px;
    }

    .spacer {
        flex: 1;
    }

    .avatar-group {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 12px;
    }

    .chat-content-body {
        flex: 1;
        display: flex;
        flex-direction: column;
        padding: 20px;
    }

    .chat-content-body-message {
        flex: 1;
        overflow-y: auto;
        padding: 0 8px;
    }

    .chat-content-body-empty {
        align-items: center;
        justify-content: center;
        gap: 24px;
    }

    .chat-content-body-title {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 12px;
        font-size: 18px;
        font-weight: 500;
        color: #333;
    }

    .title-icon {
        display: flex;
        align-items: center;
    }

    .title-text {
        font-weight: 500;
    }

    .chat-content-body-input {
        width: 70%;
        margin: 0 auto;
    }

    .chat-content-body-tip {
        margin-top: 24px;
    }

    .icon {
        width: 20px;
        height: 20px;
        padding: 4px;
        border-radius: 4px;
        transition: all 0.2s;
        cursor: pointer;
    }

    .icon:hover {
        background: rgba(0, 0, 0, 0.05);
        color: #1890ff;
    }

    .chat-content-body-title .icon {
        width: 28px;
        height: 28px;
        color: #1890ff;
        padding: 4px;
        border-radius: 6px;
        background: rgba(24, 144, 255, 0.1);
    }
</style>
