<template>
  <button @click="toggleMenuState()" :class="{'hamburger-menu-opened': state}">
    <svg width="22" height="15" viewBox="0 0 22 15" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect width="22" height="3" rx="1" fill="white"/>
      <rect y="8" width="22" height="3" rx="1" fill="white"/>
    </svg>
  </button>
</template>

<script>
export default {
  name: 'HamburgerButton',
  data () {
    return {
      // 0 => closed, 1 => opened
      state: 0
    }
  },
  mounted () {
    const self = this
    /* global $nuxt */
    // subscribe event for global toggle menu event
    /* eslint no-undef: "error" */
    $nuxt.$on('toggle-menu-global', () => {
      self.toggleMenuState()
    })
  },
  methods: {
    toggleMenuState () {
      if (this.state) {
        this.state = 0
      } else {
        this.state = 1
      }
      /* eslint no-undef: "error" */
      $nuxt.$emit('toggle-navigation-menu', this.state)
    }
  }
}
</script>

<style scoped>
button {
  border: none;
  box-sizing: border-box;
  transition: 200ms ease;
  width: 64px;
  height: 64px;
  cursor: pointer;
  top: 0;
  z-index: 7;
  background: transparent;
}

svg rect {
  transition: 250ms ease;
}

.hamburger-menu-opened svg rect:nth-child(1) {
  width: 20px;
  transform: translateX(6px) translateY(-2px) rotate(45deg);
}

.hamburger-menu-opened svg rect:nth-child(2) {
  width: 20px;
  transform: translateX(-1px) translateY(6px) rotate(-45deg);
}

.hamburger-menu-opened svg rect:nth-child(3) {
  opacity: 0;
}

</style>
