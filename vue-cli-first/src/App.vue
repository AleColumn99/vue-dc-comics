<template>
  <div id="app">
    <Title />
    <Hero />
  </div>
</template>

<script>
import Title from '@/components/Title.vue'
import Hero from '@/components/Jumbotron.vue'

export default {
  name: 'App',
  components: {
    Title,
    Hero
  }
}
</script>

<style lang="scss">
</style>
