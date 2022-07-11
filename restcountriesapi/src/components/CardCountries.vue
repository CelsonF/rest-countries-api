<template>
  <div class="d-grid grid-cards">
    <div class="card" v-for="item in itemsCard" :key="item.id">
      <img :src="item.flags.png" :alt="item.name.common"  width="60%">
      <h3> Name : {{item.name.common}} </h3>
      <div>
        <p>
          <b>
            Population: {{item.population}}
          </b>
        </p>
        <p>
          <b>
            Region: {{item.region}}
          </b>
        </p>
        <p>
          <b>
            Capital: {{item.capital}}
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
    itemsCard: {
      type: Array,
      required: false,
    },
  },
  created() {
    this.$emit('getFlags');
  },
});
</script>
<style lang="css">

.grid-cards {
grid-template: "card card card card";
}

</style>
