<template>
  <div class="believe-item">
    <img class="desktop-only" :src="image" alt="">
    <div>
      <div class="mobile-only-container">
        <img class="mobile-only" :src="image" alt="">
        <h3>{{ heading }}</h3>
      </div>
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

@media (max-width: 950px) {
  img {
    margin-right: 24px;
    width: 48px;
    height: 48px;
  }

  .desktop-only {
    display: none;
  }

  .mobile-only-container {
    display: flex;
    align-items: center;
  }

  p {
    margin-top: 16px;
    font-size: 14px;
    line-height: 25px;
  }
}

@media(min-width: 950px) {
  .mobile-only {
    display: none;
  }
}

</style>
