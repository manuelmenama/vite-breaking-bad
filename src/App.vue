<script>

import "../node_modules/@fontsource/lato/index.css";

import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';
import AppCardWrapper from './components/AppCardWrapper.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppSearch,
    AppCardWrapper
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