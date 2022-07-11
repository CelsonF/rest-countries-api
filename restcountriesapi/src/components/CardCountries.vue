<template>
  <div class="d-grid grid-cards">
    <div class="card">
      <img src="https://flagcdn.com/pe.svg" alt=""  width="100%">
      <h3> Name </h3>
      <div>
        <p>
          <b>
            Population:
          </b>
        </p>
        <p>
          <b>
            Region:
          </b>
        </p>
        <p>
          <b>
            Capital:
          </b>
        </p>
      </div>
    </div>
    <div class="card">
      <img src="https://flagcdn.com/pe.svg" alt=""  width="100%">
      <h3> Name </h3>
      <div>
        <p>
          <b>
            Population:
          </b>
        </p>
        <p>
          <b>
            Region:
          </b>
        </p>
        <p>
          <b>
            Capital:
          </b>
        </p>
      </div>
    </div>
    <div class="card">
      <img src="https://flagcdn.com/pe.svg" alt=""  width="100%">
      <h3> Name </h3>
      <div>
        <p>
          <b>
            Population:
          </b>
        </p>
        <p>
          <b>
            Region:
          </b>
        </p>
        <p>
          <b>
            Capital:
          </b>
        </p>
      </div>
    </div>
    <div class="card">
      <img src="https://flagcdn.com/pe.svg" alt=""  width="100%">
      <h3> Name </h3>
      <div>
        <p>
          <b>
            Population:
          </b>
        </p>
        <p>
          <b>
            Region:
          </b>
        </p>
        <p>
          <b>
            Capital:
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
