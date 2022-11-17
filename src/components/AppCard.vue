<script>

export default {
  name: "AppCard",
  props: {
    character: Object,
  }
}
</script>

<template>

  <div class="card">
    <img :src="character.img" alt="">

    <h3>{{character.name}}</h3>
    <h5>{{character.status}}</h5>

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