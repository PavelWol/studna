<template>
  <footer>
    <div class="fake-bg"></div>
    <div class="footer-wrapper">
      <Map />
      <div class="contact">
        <FooterItem style="cursor: pointer;" :icon="'email'" :text="'studna.spkp@gmail.com'" @click.native="sendEmail()" />
        <FooterItem style="cursor: pointer;" :icon="'phone'" :text="'+420 777 665 012'" @click.native="callPhone()" />
        <FooterItem :icon="'card'" :text="'00076589876675/2100'" />
      </div>
      <div class="copyright">
        <span>Ičo: 082 23 700</span>
        <span>Copyright © 2021 Studna zive vody️</span>
      </div>
    </div>
  </footer>
</template>

<script>
import Map from '~/components/interactive/Map'
import FooterItem from '~/components/navigation/FooterItem'

export default {
  namee: 'Footer',
  components: {
    Map,
    FooterItem,
  },
  methods: {
    sendEmail() {
      window.location.href = "mailto:studna.spkp@gmail.com"
    },
    callPhone() {
      window.location.href = "tel:+420 777 665 012"
    }
  }
}

</script>

<style scoped>

footer {
  background: #112636;
  position: relative;
}

.fake-bg {
  background: #A85846;
  position: absolute;
  top: 0;
  width: 100%;
  height: 80px;
}

.footer-wrapper {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  position: relative;
  padding-left: 24px;
  padding-right: 24px;
}

.contact {
  display: flex;
  justify-content: space-between;
  margin-top: 96px;
}

.copyright {
  text-align: center;
  margin-top: 96px;
}

span {
  font-family: Bebas Neue, sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: rgba(255, 255, 255, .32);
  letter-spacing: 0.4px;
}

.copyright span:first-child {
  margin-right: 24px;
}

@media (max-width: 950px) {
  .contact {
    flex-direction: column;
    margin-top: 32px;
  }

  span {
    font-size: 14px;
  }
}

</style>
