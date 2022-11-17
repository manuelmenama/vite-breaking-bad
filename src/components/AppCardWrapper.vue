<script>

import { store } from '../data/store';

import AppCard from './AppCard.vue';
import LoadingCompVue from './LoadingComp.vue';

export default {
  name: "AppCardWrapper",
  data() {
    return {
      store,
    }
  },
  components:{
    AppCard,
    LoadingCompVue
  }
}
</script>

<template>

  <div class="container styled">

    <div class="element-counter">
      <h5><span>{{store.charcters.length}}</span> Element found</h5>
    </div>

    <div class="card-container" v-if="store.isLoaded">
      <AppCard
        v-for="character in store.charcters"
        
        :key="character.char_id"
        :character="character"/>

      </div>
      <div v-else>

        <LoadingCompVue/>
      </div>

  </div>
  
</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

.styled{
  background-color: white;
  padding-top: 10px;
  padding-bottom: 10px;
  .card-container{
    @include flex('only');
    flex-wrap: wrap;
  }
  .element-counter{
    background-color: darken($primary-color, 5%);
    margin: 10px 10px;
    padding: 10px 20px;
  }
}

</style>