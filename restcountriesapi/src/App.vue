<template>
  <div id="app">
    <HeaderTop class="d-flex" />
    <InputSearch/>
    <CardCountries/>
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
});
</script>

<style scoped lang="css">

</style>
