<script setup lang="ts">
import { ref, computed} from 'vue'
// @ts-ignore
import MarkdownIt from 'vue3-markdown-it'
const content = `## ChatGPT 回复\n\`\`\`js\nconsole.log("Hello")\n\`\`\``
</script>

<template>
    <div>
        <MarkdownIt :source="content" />
    </div>
</template>