<template>
   <header> <AppTitle /></header>
</template>

<script>
import AppTitle from './AppTitle.vue'
export default {
    name: 'AppHero',
    components:{
        AppTitle,
    },
    data() {
        return {

        }
    }
}
</script>

<style scoped>
 header {
    background-image: url(C:\esercizi\vite-hello-world\public\jumbo.png);
    height: 200px;
 }
</style>