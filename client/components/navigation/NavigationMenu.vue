<template>
  <div :class="{'overlay': state }">
    <div :class="{'navigation-menu-wrapper': true, 'navigation-menu-opened': state}">
      <div class="navigation-menu-content-wrapper">
        <Close />
        <ul class="navigation-items">
          <li v-for="nav in navigationItems" :key="nav.name" @click="scrollInto(nav.anchor)">
            <svg width="24" height="12" viewBox="0 0 24 12" fill="none" xmlns="http://www.w3.org/2000/svg">
             <path d="M1 6L17 6" stroke="#5B2215" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="square" stroke-linejoin="round"/>
              <path d="M17 0L24 6L17 12V0Z" fill="#5B2215"/>
            </svg>
            {{ nav.name }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Close from '~/components/interactive/buttons/Close'

export default {
  name: 'NavigationMenu',
  components: {
    Close,
  },
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
  height: 549px;
  top: -100%;
  right: 0;
  background: #A85846;
  z-index: 6;
  transition: 450ms ease;
  box-shadow: 0 2px 0 0 #5B2215;
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 5;
  background: rgba(0, 0, 0, .3);
  transition: 250ms ease;
}

.navigation-items {
  display: flex;
  flex-direction: column;
  align-items: end;
}

.navigation-menu-opened {
  top: 0px;
}

.navigation-menu-content-wrapper {
  position: absolute;
  left: 50%;
  top: 48px;
  transform: translateX(-50%);
  text-align: right;
  z-index: 6;
}

ul {
  list-style: none;
  text-align: center;
  padding: 0;
  margin: 40px 0 0 0;
}

ul li {
  font-family: Bebas Neue, sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 40px;
  line-height: 40px;
  text-align: right;
  color: #5B2215;
  cursor: pointer;
  margin-top: 16px;
  text-transform: uppercase;
  transition: 250ms ease;
  position: relative;
}

ul li:first-child {
  margin-top: 0;
}

ul li:hover {
  color: #ffffff;
  transition: 250ms ease;
}

svg {
  position: absolute;
  top: 50%;
  left: -16px;
  transform: translate(-100%, -50%);
  opacity: 0;
  visibility: hidden;
  transition: 250ms ease;
}

ul li:hover svg {
  opacity: 1;
  visibility: visible;
  transition: 250ms ease;
}

@media (max-width: 950px) {
  .navigation-menu-wrapper {
    width: 100%;
    height: 55%;
  }

  .navigation-items {
    align-items: center;
    margin: 24px 0 0 0;
  }

  ul li {
    font-size: 20px;
    line-height: 22px;
  }

  .navigation-menu-content-wrapper {
    width: calc(100% - 32px);
  }

  .navigation-menu-wrapper {
    z-index: 6;
  }
}

@media (max-width: 350px) {
  .navigation-menu-wrapper {
    height: 60%;
  }
}

@media (min-width: 1920px) {
  .navigation-menu-wrapper {
    width: 30vw;
  }
}
</style>
