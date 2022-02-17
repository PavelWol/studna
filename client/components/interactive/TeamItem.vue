<template>
  <div class="team-item">
    <div class="container">
      <img :src="image" alt="">
      <h3>{{ name }}</h3>
      <p>{{ position }}</p>
    </div>
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

.team-item:first-child .container {
  margin-top: 132px;
  max-width: 267px;
}

.team-item:nth-child(2) .container {
  max-width: 235px;
  margin-top: 48px;
}

.team-item:last-child .container {
  max-width: 165px;
}

img {
  display: block;
  width: 100%;
}

h3 {
  color: #638C9F;
  margin-top: 32px;
  white-space: nowrap;
}

p {
  margin-top: 8px;
  color: rgba(255, 255, 255, .8);
}

@media (max-width: 950px) {
  p {
    font-size: 14px;
    margin-top: 0;
  }

  .team-item:first-child .container {
    margin-top: 40px;
    max-width: 205px;
  }

  .team-item:nth-child(2) .container {
    max-width: 190px;
    margin-top: 24px;
    margin-left: auto;
  }

  .team-item:last-child .container {
    max-width: 148px;
    margin-top: 24px;
    margin-right: auto;
    padding-left: 24px;
  }
}

</style>
