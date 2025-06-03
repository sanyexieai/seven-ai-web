<script setup lang="ts">
import { ref, computed} from 'vue'
// @ts-ignore
import MarkdownIt from 'vue3-markdown-it'
const content = `## ChatGPT 回复\n\`\`\`js\nconsole.log("Hello")\n\`\`\``
</script>

<template>
    <div class="chat-message">
        <MarkdownIt :source="content" class="markdown-body" />
    </div>
</template>

<style scoped>
.chat-message {
    padding: 16px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.05);
}

:deep(.markdown-body) {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 14px;
    line-height: 1.6;
    color: #333;
}

:deep(.markdown-body h1),
:deep(.markdown-body h2),
:deep(.markdown-body h3),
:deep(.markdown-body h4) {
    margin-top: 24px;
    margin-bottom: 16px;
    font-weight: 600;
    line-height: 1.25;
}

:deep(.markdown-body h1) {
    font-size: 2em;
    border-bottom: 1px solid #eaecef;
    padding-bottom: 0.3em;
}

:deep(.markdown-body h2) {
    font-size: 1.5em;
    border-bottom: 1px solid #eaecef;
    padding-bottom: 0.3em;
}

:deep(.markdown-body h3) {
    font-size: 1.25em;
}

:deep(.markdown-body h4) {
    font-size: 1em;
}

:deep(.markdown-body code) {
    padding: 0.2em 0.4em;
    margin: 0;
    font-size: 85%;
    background-color: rgba(27, 31, 35, 0.05);
    border-radius: 3px;
    font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
}

:deep(.markdown-body pre) {
    padding: 16px;
    overflow: auto;
    font-size: 85%;
    line-height: 1.45;
    background-color: #f6f8fa;
    border-radius: 6px;
    margin: 16px 0;
}

:deep(.markdown-body pre code) {
    padding: 0;
    margin: 0;
    background-color: transparent;
    border: 0;
    word-break: normal;
    white-space: pre;
}

:deep(.markdown-body p) {
    margin-top: 0;
    margin-bottom: 16px;
}

:deep(.markdown-body blockquote) {
    padding: 0 1em;
    color: #6a737d;
    border-left: 0.25em solid #dfe2e5;
    margin: 0 0 16px 0;
}

:deep(.markdown-body ul),
:deep(.markdown-body ol) {
    padding-left: 2em;
    margin-top: 0;
    margin-bottom: 16px;
}

:deep(.markdown-body table) {
    display: block;
    width: 100%;
    overflow: auto;
    margin-top: 0;
    margin-bottom: 16px;
    border-spacing: 0;
    border-collapse: collapse;
}

:deep(.markdown-body table th),
:deep(.markdown-body table td) {
    padding: 6px 13px;
    border: 1px solid #dfe2e5;
}

:deep(.markdown-body table tr) {
    background-color: #fff;
    border-top: 1px solid #c6cbd1;
}

:deep(.markdown-body table tr:nth-child(2n)) {
    background-color: #f6f8fa;
}
</style>