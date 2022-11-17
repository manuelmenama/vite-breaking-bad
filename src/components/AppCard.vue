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

    <h5>{{character.name}}</h5>
    <h6>{{character.status}}</h6>

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
  img{
    margin-bottom: 1rem;
  }
  h5{
    color: white;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  h6{
    color: white;
    margin-bottom: 1rem;
  }

}

</style>