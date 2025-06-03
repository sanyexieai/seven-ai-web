<script setup lang="ts">
import { ref } from 'vue'
</script>

<template>
  <div class="chat-input-bar">
    <input class="chat-input-bar-input" type="text" placeholder="输入消息" />
    <div class="chat-input-bar-tools">
      <div class="chat-input-bar-tools-left">
        <button class="icon-btn flat">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-tianjia"></use>
          </svg>
        </button>
        <button class="icon-btn flat">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-hulianwang"></use>
          </svg>
          <span>联网搜索</span>
        </button>
        <button class="icon-btn flat">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-code"></use>
          </svg>
          <span>代码解释器</span>
        </button>
      </div>
      <div class="chat-input-bar-tools-right">
        <button class="icon-btn circle ">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-luyinyuyin"></use>
          </svg>
        </button>
        <button class="icon-btn circle ">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-hujiao"></use>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.chat-input-bar {
  display: flex;
  flex-direction: column;
  background: #fff;
  border-radius: 32px;
  box-shadow: 0 2px 12px rgba(0,0,0,0.08);
  padding: 16px 32px 8px 32px;
  margin: 0 auto;
  width: 100%;
  max-width: 900px;
  position: relative;
}

.chat-input-bar-input {
  border: none;
  outline: none;
  background: transparent;
  font-size: 16px;
  padding: 0 0 12px 0;
  width: 100%;
  color: #222;
}
.chat-input-bar-input::placeholder {
  color: #bbb;
  font-size: 16px;
}

.chat-input-bar-tools {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.chat-input-bar-tools-left {
  display: flex;
  flex-direction: row;
  gap: 8px;
}

.chat-input-bar-tools-right {
  display: flex;
  flex-direction: row;
  gap: 12px;
}

.icon-btn {
  display: flex;
  align-items: center;
  gap: 6px;
  border: none;
  background: none;
  padding: 6px 12px;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
  color: #666;
  transition: background 0.2s, color 0.2s;
}
.icon-btn.flat:hover {
  background: #f5f5f5;
  color: #1890ff;
}
.icon-btn.flat .icon {
  color: #666;
}
.icon-btn.flat:hover .icon {
  color: #1890ff;
}
.icon-btn span {
  font-size: 14px;
  line-height: 1;
}

.icon-btn.circle {
  padding: 0;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
  display: flex;
}
.icon-btn.circle.dark {
  background: #111;
  color: #fff;
}
.icon-btn.circle.dark .icon {
  color: #fff;
}
.icon-btn.circle.dark:hover {
  background: #333;
}

.icon {
  width: 20px;
  height: 20px;
  display: inline-block;
  transition: color 0.2s;
}
</style>