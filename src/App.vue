<template>
  <AppHero/>
 <AppQuestion/>
</template>

<script>
import AppHero from './components/AppHero.vue';
import AppTitle from './components/AppTitle.vue';
import AppQuestion from './components/AppQuestion.vue';
export default {
  name: 'App',
  components: {
    AppHero,
    AppTitle,
    AppQuestion
  },
  data() {
    return {
     
    }
  },
  methods: {

  }
}
</script>

<style scoped></style>
