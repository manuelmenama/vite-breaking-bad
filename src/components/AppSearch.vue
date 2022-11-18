<script>

import {store} from '../data/store';

export default {
  name: "AppSearch",
  data() {
    return {
      store
    }
  }
}
</script>

<template>

  <div class="container input-space">
    <label for="series">Choose a series:</label>

    <select
      v-model="store.selectedSeries"
      name="series"
      id="series">
      <option value="" selected>All</option>
      <option value="breaking bad">Breaking Bad</option>
      <option value="better call saul">Better Call Saul</option>
    </select>
    <button
      @click="$emit('startFilter')">Vai!</button>
  </div>
  
</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.input-space{
  margin-bottom: 2rem;
  select{
    padding: 5px 10px;
    margin-left: 1rem;
    height: 2rem;
    background-color: lighten($color: $primary-color, $amount: 60%);
    border: 1px solid darken($color: $primary-color, $amount: 5%);
    cursor: pointer;
  }
  button{
    display: inline-block;
    background-color: lighten($color: $primary-color, $amount: 60%);
    height: 2rem;
    padding: 5px 10px;
    border: 1px solid darken($color: $primary-color, $amount: 5%);
    margin-left: 1rem;
    cursor: pointer;
  }
}

</style>