<template>
  <div class="team-item">
    <img :src="image" alt="">
    <h3>{{ name }}</h3>
    <p>{{ position }}</p>
  </div>
</template>

<script>
export default {
  name: 'TeamItem',
  props: ['image', 'name', 'position']
}
</script>

<style scoped>

.team-item {
  text-align: center;
}

.team-item:first-child {
  margin-top: 132px;
}

.team-item:nth-child(2) img {
  max-width: 235px;
  margin-top: 48px;
}

.team-item:last-child img {
  max-width: 165px;
}

img {
  display: block;
  max-width: 267px;
}

h3 {
  color: #638C9F;
  margin-top: 32px;
}

p {
  margin-top: 8px;
  color: rgba(255, 255, 255, .8);
}

</style>
