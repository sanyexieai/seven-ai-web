<script setup lang="ts">
import { ref, computed} from 'vue'

</script>

<template>
    <div>
        <div>
            <input type="text" placeholder="有什么我能帮你的吗" />
        </div>
        <div class="chat-input-tools">
            <div class="chat-input-tools-item">
                <div>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-_qi"></use>
                        </svg> 
                    </div>
                    <div>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-_qi"></use>
                        </svg> 
                        联网搜索
                    </div>
                    <div>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-_qi"></use>
                        </svg> 
                        代码解释器
                    </div>
            </div>
            <div class="chat-input-tools-item">
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
        </div>
    </div>
</template>

<style scoped>
.chat-input-tools {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
.chat-input-tools-item {
    display: flex;
    flex-direction: row;
}
</style>