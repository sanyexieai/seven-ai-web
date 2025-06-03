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
                <div style="display: flex;flex-direction: row;align-items: center;">
                    <div>llama3.2:latest</div>
                    <div>
                        <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                        </svg>  
                    </div>
                    <div>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-_qi"></use>
                        </svg>  
                    </div>
                </div>
                <div >
                    <div style="text-align: left;">设为默认</div>
                </div>
            </div>
            <div class="chat-content-header-avatar">
                <div style="flex: 1;"></div>
                <div style="display: flex;flex-direction: row;align-items: center;">
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
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
                <div>
                    <svg class="icon" aria-hidden="true">
                        <use xlink:href="#icon-_qi"></use>
                    </svg>  
                </div>
                <div>llama3.2:latest</div>
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
    .chat-content-header-model > div:first-child {
        font-weight: 500;
        color: #333;
    }
    .chat-content-header-model > div:last-child {
        font-size: 13px;
        color: #666;
        cursor: pointer;
        transition: color 0.2s;
    }
    .chat-content-header-model > div:last-child:hover {
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
        gap: 8px;
        font-size: 18px;
        font-weight: 500;
        color: #333;
    }
    .chat-content-body-title .icon {
        width: 24px;
        height: 24px;
        color: #1890ff;
    }
    .chat-content-body-input {
        margin-top: 16px;
    }
    .chat-content-body-tip {
        margin-top: 24px;
    }
</style>
