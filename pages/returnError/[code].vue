<script setup>
definePageMeta({
    middleware: 'redirect'
})
const nuxtApp = useNuxtApp()
const error = (code) => {
    const errorObj = new Error(`Error ${code}`)
    // errorObj.statusCode = code
    // nuxtApp.ssrContext.nuxt.error = errorObj
    const router = useNuxtApp().$router

    // redirect('/oops/' + code)

    // router.replace({
    //     path: '/oops/' + code,

    // })
}
const route = useRoute()
const code = route.params.code
error(code)
</script>