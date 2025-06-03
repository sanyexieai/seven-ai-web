<script setup lang="ts">
import { ref, computed } from 'vue'

const props = defineProps<{ name: string }>()

// 头像显示字符 取name的第一个字符
const avatar = computed(() => {
    return props.name.charAt(0).toUpperCase()
})

// 根据名字生成固定的背景色
const avatarStyle = computed(() => {
    const colors = [
        '#1890ff', // 蓝色
        '#52c41a', // 绿色
        '#faad14', // 黄色
        '#f5222d', // 红色
        '#722ed1', // 紫色
        '#13c2c2', // 青色
        '#eb2f96', // 粉色
        '#fa8c16', // 橙色
    ]
    const index = props.name.charCodeAt(0) % colors.length
    return {
        backgroundColor: colors[index]
    }
})
</script>

<template>
    <div class="avatar-wrapper">
        <div class="avatar" :style="avatarStyle">{{ avatar }}</div>
    </div>
</template>

<style scoped>
.avatar-wrapper {
    display: inline-flex;
    align-items: center;
    justify-content: center;
}

.avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    font-weight: 500;
    font-size: 16px;
    transition: all 0.3s;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.avatar:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}
</style>

