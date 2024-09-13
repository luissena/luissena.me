<template>
    <footer class="max-w-2xl mx-auto ">

        <section>
            <div class="w-[50px] h-[1px] bg-gray-200 dark:bg-gray-700 mx-auto my-10"></div>
            <p>Encontre-me no</p>
            <ul class="flex gap-3 text-lg my-3">
                <li v-for="e in findMeList">
                    <FindMe :label="e.label" :icon="e.icon" :url="e.url" />
                </li>
            </ul>
            <p>Ou me manda um email em <span class="tracking-widest">hi@luissena.dev</span>
            </p>
        </section>

        <p class="text-gray-300 my-14 text-sm dark:text-gray-600">
            <a class="border-b border-gray-100 hover:border-gray-300 dark:border-gray-900 dark:hover:border-gray-600 duration-200"
                href="https://creativecommons.org/licenses/by-nc-sa/4.0/" target="_blank">CC BY-NC-SA
                4.0
            </a> 2024-PRESENT © Luis Sena
        </p>
    </footer>
</template>

<script setup lang="ts">
import type { FindMeProps } from './FindMe.vue';


const findMeList: FindMeProps[] = [
    { label: "GitHub", icon: "mdi:github", url: "https://github.com/luissena" },
    { label: "Linkedin", icon: "mdi:linkedin", url: "https://www.linkedin.com/in/oluissena/" }
]

</script>