<template>
  <div :class="{'navigation-menu-wrapper': true, 'navigation-menu-opened': state}">
    <div class="navigation-menu-content-wrapper">
      <ul class="navigation-items">
        <li v-for="nav in navigationItems" :key="nav.name" @click="scrollInto(nav.anchor)">{{ nav.name }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavigationMenu',
  data () {
    return {
      // state 0 => closed, state 1 => opened
      state: 0,
      navigationItems: this.$store.state.navigationItems
    }
  },
  mounted () {
    // helper variable
    const self = this
    // subscribe events for opening the menu
    /* global $nuxt */
    /* eslint no-undef: "error" */
    $nuxt.$on('toggle-navigation-menu', (state) => {
      self.state = state
    })
  },
  methods: {
    scrollInto(id) {
      document.getElementById(id).scrollIntoView({behavior: 'smooth'})
      $nuxt.$emit('toggle-menu-global', false)
    }
  }
}
</script>

<style scoped>

.navigation-menu-wrapper {
  position: fixed;
  width: 550px;
  height: 55%;
  top: -100%;
  right: 0;
  background: #000000;
  z-index: 6;
  transition: 450ms ease;
}

.navigation-menu-opened {
  top: 0px;
}

.navigation-menu-content-wrapper {
  position: absolute;
  left: 50%;
  top: 25%;
  width: calc(100% - 192px);
  transform: translateX(-50%);
}

ul {
  list-style: none;
  text-align: center;
  padding: 0;
}

ul li {
  font-family: "Gilroy", sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 180%;
  color: #FFFFFF;
  margin-right: 28px;
  margin-left: 28px;
  cursor: pointer;
  margin-top: 24px;
}

ul li:first-child {
  margin-top: 0;
}

@media (max-width: 500px) {
  .navigation-menu-wrapper {
    width: 100%;
  }

  .navigation-menu-content-wrapper {
    width: calc(100% - 32px);
  }

  .navigation-menu-wrapper {
    z-index: 6;
  }
}
</style>
