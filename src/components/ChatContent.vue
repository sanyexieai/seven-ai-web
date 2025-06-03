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
    }
    .chat-content-header {
        height: 50px;
        display: flex;
        flex-direction: row;
    }
    .chat-content-header-model {
        flex: 1;
        display: flex;
        flex-direction: column;
    }
    .chat-content-header-avatar{
        flex: 1;
        display: flex;
        flex-direction: row;
    }
    .chat-content-body {
        flex: 1;
        display: flex;
        flex-direction: column;
    }
    .chat-content-body-message {
        flex: 1;
    }
    .chat-content-body-empty {
        align-items: center;
        justify-content: center;
    }
    .chat-content-body-title {
        display: flex;
        flex-direction: row;
        align-items: center;
    }
</style>
