<template>
    <label for="search-countries" class="px-1 pt-2 d-flex justify-content-center">
        <input
            class="input-search"
            id="search-countries"
            type="search"
            placeholder="Search for a country..."
        >
    </label>
</template>
<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'input-search',
});

</script>

<style>
input#search-countries::placeholder {
color:rgba(224, 224, 224, 0.879);
}

.input-search {
  border-radius: 0.3rem;
  border:none;
  box-shadow:0px 0px 10px hsl(0deg 0% 83%);
  background-color: var(--background-color-primary);
  padding: 1rem;

}

</style>
