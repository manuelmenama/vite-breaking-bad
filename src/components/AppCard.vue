<script>
export default {
  name: "AppCard"
}
</script>

<template>

  <div class="card">
    <img src="/breaking_bad_logo.svg" alt="">

    <h3>name</h3>
    <h5>Role</h5>

  </div>
  
</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.card{
  color: black;
  width: calc(100% / 5 - 20px);
  background-color: $primary-color;
  margin: 10px;
  text-align: center;
  h3{
    color: white;
    text-transform: uppercase;
  }
  h5{
    color: white;
  }

}

</style>