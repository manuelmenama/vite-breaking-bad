<script>

export default {
  name: "AppHeader"
}
</script>

<template>

  <header>

    <div class="logo">
      <img src="/breaking_bad_logo.svg" alt="">
    </div>

    <h1>BREAKING VUE, BADLY</h1>

  </header>
  
</template>


<style lang="scss" scoped>

@use '../styles/partials/mixin.scss' as *;

header{
  @include flex('align-center');

  margin-bottom: 2rem;
}
.logo{
  background-color: white;
  display: inline-block;
  padding: 5px 10px;
  margin-right: 1rem;
  img{
    height: 70px;
  }
}

</style>