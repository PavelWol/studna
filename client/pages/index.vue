<template>
  <div class="wrapper">
    <Hero class="hero" />
    <CurrentInfo />
  </div>
</template>

<script>

import Hero from '~/components/sections/Hero'
import CurrentInfo from '~/components/sections/CurrentInfo'


export default {
  components: {
    Hero,
    CurrentInfo,
  },
}
</script>

<style>

body {
  margin: 0;
}

h1, h2, h3, h4 {
  margin-top: 0;
  margin-bottom: 0;
  color: #ffffff;
  font-family: Bebas Neue, sans-serif;
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
  font-family: Marcellus, sans-serif;

}

.hero {
  position: relative;
  padding-bottom: 270px;
}

</style>
