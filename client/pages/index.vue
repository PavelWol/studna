<template>
  <div class="wrapper">
    <Hero class="hero" />
  </div>
</template>

<script>

import Hero from '~/components/sections/Hero'

export default {
  components: {
    Hero,
  },
}
</script>

<style>

body {
  margin: 0;
}

h1, h2, h3 {
  margin-top: 0;
  margin-bottom: 0;
  color: #ffffff;
}

h1 {
  font-size: 112px;
}

h2 {
  font-size: 96px;
}

h3 {
  font-size: 40px;
}

p {
  margin: 0;
  font-weight: normal;
  font-size: 18px;
  line-height: 29px;
  color: #ffffff;
}

.hero {
  position: relative;
  padding-top: 120px;
  padding-bottom: 270px;
}

</style>
