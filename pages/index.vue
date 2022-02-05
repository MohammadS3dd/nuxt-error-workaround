<template>
    <div class="flex flex-col">
        <button @click="error(404)">404</button>
        <button @click="error(100)">100</button>
    </div>
</template>
<script setup>
const error = (code) => {
    const errorObj = new Error(`Error ${code}`)
    errorObj.statusCode = code
    const router = useNuxtApp().$router

    router.replace({
        path: '/oops/' + code,

    })
}
</script>