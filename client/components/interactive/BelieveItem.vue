<template>
  <div class="believe-item">
    <img :src="image" alt="">
    <div>
      <h3>{{ heading }}</h3>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamItem',
  props: ['image', 'heading', 'text']
}
</script>

<style scoped>

.believe-item {
  display: flex;
  align-items: flex-start;
}

img {
  margin-right: 40px;
}

h3 {
  text-transform: uppercase;
  color: #5B2215;
}

p {
  color: rgba(255, 255, 255, .8);
  margin-top: 24px;
  line-height: 32px;
}

</style>
