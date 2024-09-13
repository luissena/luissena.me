<template>
    <a class="flex items-center gap-1 border-b border-gray-200 hover:border-gray-500 dark:text-gray-200 dark:border-gray-700 dark:hover:border-gray-200 duration-200"
        :href="url" target="_blank">
        <Icon :name="icon" />
        {{ label }}
    </a>
</template>

<script setup lang="ts">

export type FindMeProps = {
    label: string;
    url: string;
    icon: string;
}

const { label, icon, url } = defineProps<FindMeProps>()

</script>
