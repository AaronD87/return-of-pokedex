<template>
    <ul>
    <Pokemon v-for="pokemon in pokemons"
      v-bind:key="pokemon.name"
      v-bind:pokemon="pokemon"/>
  </ul>
</template>

<script>
import Pokemon from './Pokemon.vue';
export default {
    props: {
        pokemons: Array
    },
    components: {
        Pokemon
    }
};
</script>

<style>
ul {
    margin-top: 40px;
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-row-gap: 20px;
    grid-column-gap: 10px;
    list-style: none;
}
</style>
