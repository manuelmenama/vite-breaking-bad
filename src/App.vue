<script>

import "../node_modules/@fontsource/lato/index.css";
import {store} from './data/store'

import axios from 'axios';

import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';
import AppCardWrapper from './components/AppCardWrapper.vue';

export default {
  name: "App",
  data(){
    return {
      store
    }
  },
  components: {
    AppHeader,
    AppSearch,
    AppCardWrapper
  },
  methods:{
    getApiCaracters(){
      store.isLoaded = false;
      axios.get(store.apiUrl)
    .then(function( response ){

      store.charcters = response.data

      console.log(response.data);
      store.isLoaded=true;
    })
    .catch(function(error){
      console.log(error);
    })
    }
  },
  mounted(){

    this.getApiCaracters();
  }
}
</script>

<template>

  <AppHeader/>  

  <main>

    <AppSearch/>
    <AppCardWrapper/>

  </main>
  
</template>

<style lang="scss">

@use "./styles/general.scss";

</style>