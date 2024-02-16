<template>
    <div >
      <PokeCard v-for="pokemon of pokemons" :key="pokemon" v-bind:pokemon="pokemon" @click="selectedPokemon = pokemon">
      </PokeCard>
      <!-- PokeModal v-if="selectedPokemon"></PokeModal --> 
    </div>
  </template>
  <script>
  import PokeCard from './PokeCard.vue'
  import json_pokemons from '@/assets/pokemon.json'
  
  export default {
    name: 'PokeList',
    components: {
      PokeCard
    },
    data() {
      return {
          pokemons: json_pokemons,
          selectedPokemon: json_pokemons[0],
          open :false,
      }
    },
    methods: {
      mamethode() {
        console.log("On m'a clické dessus !!!")
      }
    },
    created(){
    
    }
  }
  </script>
  <style scoped>

  </style>