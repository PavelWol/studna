<template>
  <div>
    <div class="bg"></div>
    <Navigation />
    <div class="wrapper">
      <div class="info">
        <h1>Jsme otevřená křesťanská církev</h1>
        <div class="container">
          <p style="display: none">
            „Kdo se však napije vody, kterou mu dám já, nebude žíznit už nikdy.
            Voda, kterou mu dám, se v něm stane pramenem vody tryskající k věčnému životu.“
          </p>
          <div class="socials">
            <SocButton :title="'AKTUALITY'" :icon="'facebook'" style="cursor: pointer;" @click.native="openWebsite('https://www.facebook.com/studnaspkp')" />
            <SocButton :title="'kázání'" :icon="'youtube'" />
            <SocButton :title="'Fotky'" :icon="'instagram'" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SocButton from '~/components/interactive/buttons/SocButton'
import Navigation from '~/components/navigation/Navigation'

export default {
  name: 'Hero',
  components: {
    Navigation,
    SocButton
  },
  methods: {
    openWebsite (url) {
      window.open(url, '_blank')
    },
  }
}
</script>

<style scoped>

.info {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 96px;
  padding-left: 24px;
  padding-right: 24px;
  text-align: center;
  flex-direction: column;
}

h1 {
  max-width: 600px;
}

p {
  font-size: 24px;
  line-height: 43px;
  color: rgba(255, 255, 255, .8);
}

.container {
  max-width: 425px;
}

.bg {
  background-image: url("~assets/images/hero_img.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  background-position: center;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
}

.socials {
  display: flex;
  margin-top: 48px;
}

.wrapper {
  position: relative;
}

@media (max-width: 950px) {
  .info {
    flex-direction: column;
    max-width: 500px;
    padding-top: 40px;
  }

  h1 {
    max-width: 273px;
    line-height: 67px;
  }

  p {
    font-size: 18px;
    line-height: 32px;
  }

  .bg {
    background-size: 200% 100%;
    background-position: inherit;
  }

  .container {
    max-width: unset;
    margin-top: 16px;
    width: 100%;
  }

  .socials {
    margin-top: 80px;
    justify-content: center;
  }
}

@media (max-width: 350px) {
  .socials {
    flex-wrap: wrap;
  }

  .socials ::v-deep .soc:last-child {
    margin-top: 8px;
  }
}

</style>
