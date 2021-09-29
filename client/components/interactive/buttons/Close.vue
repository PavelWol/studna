<template>
  <button class="close" @click="toggleMenuState()">
    <svg width="32" height="32" viewBox="0 0 22 15" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect width="32" height="2" rx="1" fill="white"/>
      <rect y="6" width="32" height="2" rx="1" fill="white"/>
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
        this.state = 1
      } else {
        this.state = 0
      }
      /* eslint no-undef: "error" */
      $nuxt.$emit('toggle-navigation-menu', this.state)
      $nuxt.$emit('hamburger-menu-opened', this.state)
    }
  }
}
</script>

<style scoped>
button {
  border: none;
  box-sizing: border-box;
  transition: 200ms ease;
  width: 32px;
  height: 32px;
  cursor: pointer;
  top: 0;
  z-index: 7;
  background: transparent;
  padding: 0;
  padding-right: 24px;
  box-sizing: content-box;
}

svg {
  width: 32px;
  height: 32px;
}

svg rect {
  transition: 250ms ease;
}

.close svg rect:nth-child(1) {
  transform: translateX(2px) translateY(-3px) rotate(45deg);
}

.close svg rect:nth-child(2) {
  transform: translateX(-3px) translateY(12px) rotate(-45deg);
}

@media( max-width: 950px) {
  .close svg rect {
    width: 20px;
  }

  .close svg rect:nth-child(1) {
    transform: translateX(3px) translateY(0) rotate(45deg);
  }

  .close svg rect:nth-child(2) {
    transform: translateX(-3px) translateY(10px) rotate(-45deg);
  }
}

</style>
