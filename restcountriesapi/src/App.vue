<template>
  <div id="app">
    <HeaderTop class="d-flex" />
    <InputSearch />
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
      inputValue: '',
    };
  },
  methods: {
    async loadFlags() {
      try {
        const searchAllFlags = 'https://restcountries.com/v3.1/all';

        const request = new Request(searchAllFlags);

        const response = await fetch(request);
        this.allFlagsObj = await response.json();
      } catch (error) {
        console.log(error);
      }
    },
  },
});
</script>

<style scoped lang="css">
</style>
