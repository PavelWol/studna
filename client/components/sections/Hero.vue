<template>
  <div>
    <div class="bg"></div>
    <Navigation />
    <div class="wrapper">
      <div class="info">
        <h1>Jsme otevřená křesťanská církev</h1>
        <div>
          <p>
            „Kdo se však napije vody, kterou mu dám já, nebude žíznit už nikdy.
            Voda, kterou mu dám, se v něm stane pramenem vody tryskající k věčnému životu.“
          </p>
          <div class="socials">
            <SocButton :title="'AKTUALITY'" :icon="'facebook'" />
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
}

.wrapper {
  position: relative;
}

</style>
