<template>
  <div id="app">
    <HeaderTop class="d-flex" />
    <InputSearch/>
    <CardCountries @getFlags="loadFlags" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

import HeaderTop from './components/HeaderTop.vue';
import InputSearch from './components/InputSearch.vue';
import CardCountries from './components/CardCountries.vue';

export default Vue.extend({
  name: 'App',
  components: {
    HeaderTop,
    InputSearch,
    CardCountries,
  },
  data() {
    return {
      allFlagsObj: [],
    };
  },
  methods: {
    async loadFlags() {
      const searchAllFlags = 'https://restcountries.com/v3.1/all';

      const request = new Request(searchAllFlags);

      const response = await fetch(request);
      const allData = await response.json();

      const result = allData.map(
        (
          flags:
            {
              name: { common: string; },
              capital: Array<string>,
              region: string,
              population: string
            },

        ) => [
          flags.name.common,
          flags.capital,
          flags.region,
          flags.population,
        ],
      );

      console.log(result);
    },
  },
});
</script>

<style scoped lang="css">

</style>
