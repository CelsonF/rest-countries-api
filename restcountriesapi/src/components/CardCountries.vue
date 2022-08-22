<template>
  <div class="d-grid grid-cards">
    <div class="card" v-for="item in itemsCard" :key="item.id">
      <img :src="item.flags.png" :alt="item.name.common" width="100%">
      <h3>Name :{{ item.name.common }} </h3>
      <div>
        <p>
          <b>
            Population: {{ item.population }}
          </b>
        </p>
        <p>
          <b>
            Region: {{ item.region }}
          </b>
        </p>
        <p>
          <b>
            Capital:
            {{ item.capital ? item.capital.join(', ') : item.capital }}

          </b>
        </p>
      </div>
    </div>
  </div>
</template>
<script lang="ts" >
import Vue from 'vue';

export default Vue.extend({
  name: 'card-countries',
  props: {
    itemsCard: Array,
  },
  created() {
    this.$emit('getFlags');
  },
});
</script>

<style lang="css">
.grid-cards {
  grid-template: "card card card card";
  column-gap: 3rem;
  row-gap: 3rem;
  padding-right: 5rem;
  padding-left: 5rem;
  padding-top: 3rem;
}
</style>
