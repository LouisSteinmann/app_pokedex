<template>
  <div>
    <header>
      <img src="./assets/logo.png" alt="">
    </header>
    <main>
      <PokeList />
    </main>
  </div>
</template>

<script>
import PokeList from './components/PokeList.vue'

export default {
  name: 'App',
  components: {
    PokeList
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-around;
}
</style>
