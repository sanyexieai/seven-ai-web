<script setup lang="ts">
import { ref, computed} from 'vue'

const props = defineProps<{ name: string }>()
//头像显示字符 取name的第一个字符
const avatar = computed(() => {
    return props.name.charAt(0)
})
</script>

<template>
    <div>
        <div class="avatar">{{ avatar }}</div>
    </div>
</template>

<style scoped>
.avatar {
    width: 24px;
    height: 24px;
    border-radius: 50%;
    text-align: center;
    color: #fff;
    background-color: orange;
}
</style>

