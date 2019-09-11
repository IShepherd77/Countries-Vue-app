<template>
  <article class="ianhead" v-if="country">
    <p>Name: {{ country.name }}</p>
    <p>Capital: {{ country.capital }}</p>
    <p>Population: {{country.population }}</p>
    <img class="flag" v-bind:src="country.flag" alt="Flag">
  </article>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
  .flag {
    width: 100px;
    border: 1px solid black;
  }

  p {
    font-weight: bold;
  }

</style>
