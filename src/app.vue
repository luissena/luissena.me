<template>
  <NuxtPage />
</template>

<style>
:root {
  @apply dark:bg-gray-950 bg-gray-50 dark:text-slate-50 font-['Inter']
}

p, li {
  @apply dark:text-gray-400 text-gray-500 leading-6
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  @apply dark:bg-gray-950 bg-gray-50;
}

::-webkit-scrollbar-thumb {
  @apply dark:bg-gray-900 bg-gray-200;
}

::-webkit-scrollbar-thumb:hover {
  @apply dark:bg-gray-800 bg-gray-300;
}
</style>
