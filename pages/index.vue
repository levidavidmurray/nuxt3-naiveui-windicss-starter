<template>
    <div class="p-6 mx-auto max-w-screen-sm">
        <h1 class="text-center">Nuxt3-NaiveUI-WindiCSS Starter</h1>
        <n-divider />
        <div class="pt-4">
            <div class="flex text-3xl justify-center">
                <a href="https://v3.nuxtjs.org/" target="_blank" class="mr-4">
                    <Icon name="logos:nuxt-icon" />
                </a>
                <a href="https://www.naiveui.com/en-US/os-theme" target="_blank" class="mr-4">
                    <Icon name="logos:naiveui" />
                </a>
                <a href="https://windicss.org/" target="_blank">
                    <Icon name="logos:windi-css" />
                </a>
            </div>
            <h2>Naive UI</h2>
            <div class="pt-4">
                <div class="flex">
                    <n-input style="max-width: 256px;" class="mr-4" v-model:value="inputValue"
                        placeholder="Give me something to say!" />
                    <n-button @click="displayMessage">Say It</n-button>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { NButton, NInput, NDivider, useMessage } from 'naive-ui'

const inputValue = ref(null)

const message = useMessage()

const displayMessage = () => {
    message.info(inputValue.value || 'Give me something to say!')
}

</script>

<style>
body {
    /* Light */
    @apply bg-neutral-50 text-neutral-900;

    /* Dark */
    @apply dark: bg-neutral-900 dark:text-neutral-100;
}

h1 {
    @apply text-4xl font-extrabold;
}

h2 {
    @apply text-xl font-semibold;
}
</style>
