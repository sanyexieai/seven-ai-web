<script setup lang="ts">
import { ref } from 'vue'

const tips = [
    {
        title: '基础功能',
        items: [
            '你可以问我任何问题',
            '我可以帮你写代码',
            '我可以帮你分析数据',
            '我可以帮你写文章'
        ]
    },
    {
        title: '高级功能',
        items: [
            '联网搜索最新信息',
            '代码解释和优化',
            '多语言翻译',
            '数学计算和公式推导'
        ]
    }
]
</script>

<template>
    <div class="chat-tip">
        <div class="chat-tip-title">你可以这样问我</div>
        <div class="chat-tip-content">
            <div v-for="(group, index) in tips" :key="index" class="tip-group">
                <div class="tip-group-title">{{ group.title }}</div>
                <div class="tip-group-items">
                    <div v-for="(item, itemIndex) in group.items" :key="itemIndex" class="tip-item">
                        {{ item }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.chat-tip {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    padding: 24px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.chat-tip-title {
    font-size: 18px;
    font-weight: 500;
    color: #333;
    margin-bottom: 24px;
    text-align: center;
}

.chat-tip-content {
    display: flex;
    gap: 32px;
    justify-content: center;
}

.tip-group {
    flex: 1;
    max-width: 360px;
}

.tip-group-title {
    font-size: 16px;
    font-weight: 500;
    color: #666;
    margin-bottom: 16px;
    padding-bottom: 8px;
    border-bottom: 1px solid #f0f0f0;
}

.tip-group-items {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.tip-item {
    padding: 12px 16px;
    background: #fafafa;
    border-radius: 6px;
    color: #666;
    font-size: 14px;
    transition: all 0.3s;
    cursor: pointer;
}

.tip-item:hover {
    background: #f0f0f0;
    color: #1890ff;
    transform: translateY(-1px);
}
</style>
