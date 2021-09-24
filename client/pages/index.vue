<template>
  <div class="wrapper">
    <Hero class="hero" />
    <CurrentInfo />
    <Description class="description" />
    <Events class="events" />
    <Team class="team" />
    <WeBelieve class="we-believe" />
    <Footer class="footer" />
  </div>
</template>

<script>

import Hero from '~/components/sections/Hero'
import CurrentInfo from '~/components/sections/CurrentInfo'
import Description from '~/components/sections/Description'
import Events from '~/components/sections/Events'
import Team from '~/components/sections/Team'
import WeBelieve from '~/components/sections/WeBelieve'
import Footer from '~/components/navigation/Footer'


export default {
  components: {
    Hero,
    CurrentInfo,
    Description,
    Events,
    Team,
    WeBelieve,
    Footer,
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
  font-weight: 500; /* ?? */
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

.description {
  padding-top: 170px;
}

.events {
  padding-top: 140px;
}

.team {
  padding-top: 96px;
  padding-bottom: 220px;
}

.we-believe {
  padding-bottom: 250px;
}

.footer {
  padding-bottom: 56px;
}

@media (max-width: 950px) {
  h1 {
    font-size: 64px !important;
  }

  h2 {
    font-size: 48px !important;
  }

  h3 {
    font-size: 32px !important;
  }

  h4 {
    font-size: 18px !important;
  }
}

</style>
