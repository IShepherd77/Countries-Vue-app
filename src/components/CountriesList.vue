<template>
  <div id="test">
    <ol>
      <list-component v-for="(country, index) in countries" v-bind:country="country"
      v-bind:key="index"></list-component>
    </ol>
  </div>
</template>

<script>
import ListComponent from './ListComponent.vue';

export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "list-component": ListComponent
  }
}
</script>

<style lang="css" scoped>
#test {
  background-color: lightgrey;
  border: 1px solid black;
  margin-right: 750px;
}

ol {
  font-weight: bold;
}
</style>
