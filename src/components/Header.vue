<template>
    <header class="py-5 flex items-center justify-between">
        <h1 class="text-4xl font-extrabold">Luis Sena</h1>

        <div>
            <Icon @click="handleTheme('light')" class="hidden dark:flex text-gray-500 cursor-pointer" :size="35"
                name="material-symbols-light:dark-mode-outline" />
            <Icon @click="handleTheme('dark')" class="text-gray-400 flex dark:hidden cursor-pointer" :size="35"
                name="material-symbols-light:sunny-outline" />
        </div>
    </header>
</template>

<script setup lang="ts">

if (process.client) {
    const actualThemeChosen = localStorage.getItem("theme")
    const systemPreferenceDark = !('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches

    if (actualThemeChosen === 'dark' || systemPreferenceDark) {
        document.documentElement.classList.add('dark')
    } else {
        document.documentElement.classList.remove('dark')
    }
}

function handleTheme(themeChosen: "dark" | "light") {
    localStorage.setItem("theme", themeChosen)
    document.documentElement.classList.add(themeChosen)

    switch (themeChosen) {
        case 'dark':
            document.documentElement.classList.remove('light')
            break
        case 'light':
            document.documentElement.classList.remove('dark')
            break

    }

}
</script>
