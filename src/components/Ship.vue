<template>
    <a class="bg-gray-200 hover:bg-gray-300 dark:bg-gray-900 dark:hover:bg-gray-700 dark:text-gray-400 text-sm  duration-200 p-1 rounded-md  flex items-center gap-1 w-fit "
        :href="url" target="_blank">

        <img class="h-3" :src="thumb" />
        {{ label }}
    </a>
</template>

<script setup lang="ts">

type ShipProps = {
    label: string;
    url: string
    thumb: string
}

const { url, label } = defineProps<ShipProps>()
</script>