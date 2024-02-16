<template>
  <div class = 'background'>
    <header>
        <div class = 'logo'>
          <img src="./assets/logo.png" alt="">
        </div>
    </header>
    <main>
        <div>
      <PokeList />
        </div>
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
.background{
background-image: url('./assets/bg.png');
}

.logo{
    display: block;
    width: 40vw; 
    margin-top: 20px;
    margin-bottom: 50px;
}

.logo img{
  width: 100%;
}
</style>
