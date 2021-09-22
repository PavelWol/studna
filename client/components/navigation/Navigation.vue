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
}

.navigation-items {
  padding-left: 0;
}

li {
  list-style-type: none;
  display: inline-block;
  font-family: "Nunito", sans-serif;
  font-weight: normal;
  font-size: 20px;
  line-height: 27px;
  letter-spacing: 0.01em;
  margin-left: 32px;
  cursor: pointer;
  position: relative;
}

li:last-of-type {
  padding: 14px 32px;
  border: 2px solid #FFFFFF;
  border-radius: 0 0 0 24px;
}

.blur {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-bottom-left-radius: 16px;
  border: 2px solid #ffffff;
  background: transparent;
  filter: blur(8px);
  z-index: -1;
  opacity: 0;
  visibility: hidden;
  transition: 250ms ease;
}

li:hover .blur {
  opacity: 1;
  visibility: visible;
  transition: 250ms ease;
}

li:hover {
  text-shadow: 1px 0 8px rgba(255, 255, 255, 1);
}

</style>
