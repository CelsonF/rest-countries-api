<template>
  <div id="app">
    <HeaderTop class="d-flex" />
    <InputSearch/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HeaderTop from './components/HeaderTop.vue';
import InputSearch from './components/InputSearch.vue';

export default Vue.extend({
  name: 'App',
  components: {
    HeaderTop,
    InputSearch,
  },
});
</script>

<style scoped lang="css">

</style>
