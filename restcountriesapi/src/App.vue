<template>
  <div id="app">
    <HeaderTop class="d-flex" />
    <InputSearch/>
    <CardCountries @getFlags="loadFlags" :itemsCard="allFlagsObj" />
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
      this.allFlagsObj = await response.json();
    },
  },
});
</script>

<style scoped lang="css">

</style>
