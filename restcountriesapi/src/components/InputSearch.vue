<template>
    <div class="d-flex w-full justify-content-between flex-direction search-row ">
      <label for="search-countries" class="w-full d-flex ">
          <input
              class="input-search"
              id="search-countries"
              type="search"
              placeholder="Search for a country..."
          >
      </label>
      <label for="region" class="d-flex justify-content-end">
        <select name="regions" id="region" class="select-regions">
          <option value="none" selected disabled hidden >Filter by Region</option>
          <option value="af">Africa</option>
          <option value="am">America</option>
          <option value="as">Asia</option>
          <option value="eu">Europe</option>
          <option value="oc">Oceania</option>
        </select>
      </label>
    </div>
</template>
<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'input-search',
});

</script>

<style>
input#search-countries::placeholder {
color:var(--text-secondary-color);
}

.input-search {
  border-radius: 0.3rem;
  border:none;
  box-shadow:0px 0px 10px rgb(236, 236, 236);
  background-color: var(--background-color-primary);
  padding: 1rem;
  width: 100%;
}

.select-regions {
  border-radius: 0.3rem;
  border:none;
  box-shadow:0px 0px 10px rgb(236, 236, 236);
  background-color: var(--background-color-primary);
  padding: 1rem;
}

</style>
