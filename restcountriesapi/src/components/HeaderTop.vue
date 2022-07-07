<template>
  <div class="navbar justify-content-between">
    <h1 class="title-header"> Where in the World? </h1>
    <div>
      darkmode
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'header-top',
});
</script>

<style>
.navbar {
  background-color: var(--background-color-primary);
  box-shadow:1px -4px 10px var(--text-secondary-color);
  padding: 2rem 1rem;
}

.title-header {
  font-size: 1rem;
  font-weight: 800;
}
</style>
