<script setup>
definePageMeta({
    middleware: 'redirect'
})
const nuxtApp = useNuxtApp()
const error = (code) => {
    const errorObj = new Error(`Error ${code}`)
    const router = useNuxtApp().$router


}
const route = useRoute()
const code = route.params.code
error(code)
</script>