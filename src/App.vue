<template>
  <div id="app">
    <h1>Taxonomy info!</h1>
    <div v-if="sport && sport.title">
      {{ sport.title }}
    </div>
    <div v-else>
      No Data found!
    </div>
  </div>
</template>

<script>
import TaxonomyQuery from "../queries/taxonomy.graphql";
export default {
  name: "App",
  data() {
    return {
      sport: [],
    };
  },
  apollo: {
    sport: TaxonomyQuery,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
