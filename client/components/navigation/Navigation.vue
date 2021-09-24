<template>
  <div class="nav-container">
    <nav>
      <p>STUDNA <br /> ŽIVÉ VODY</p>
      <img class="logo" src="~/assets/images/logo.svg" />
      <HamburgerButton class="ham-btn" />
    </nav>
    <NavigationMenu />
  </div>
</template>

<script>
import NavigationMenu from '~/components/navigation/NavigationMenu'
import HamburgerButton from '~/components/interactive/buttons/HamburgerButton'

export default {
  name: 'Navigation',
  components: {
    NavigationMenu,
    HamburgerButton,
  },
  methods: {
    scrollInto(id) {
      document.getElementById(id).scrollIntoView({behavior: 'smooth'})
    }
  }
}
</script>

<style scoped>

.logo {
  width: 80px;
}

.nav-container {
  width: 100%;
  padding-top: 48px;
}

nav {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-between;
  padding-left: 24px;
  padding-right: 24px;
}

p {
  font-family: Bebas Neue, sans-serif;
  font-size: 24px;
  text-align: right;
}

@media (max-width: 950px) {
  p {
    font-size: 18px;
    line-height: 19px;
  }
}

</style>
