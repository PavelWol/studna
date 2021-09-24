<template>
  <div class="believe-bg">
    <div class="believe-wrapper">
      <h2>V co věříme</h2>
      <div class="believe-container">
        <BelieveItem v-for="item in believes" :key="item.heading" :image="require('/assets/images/' + item.image)" :heading="item.heading" :text="item.text" />
      </div>
    </div>
  </div>
</template>

<script>
import BelieveItem from '~/components/interactive/BelieveItem'

export default {
  name: 'Team',
  components: {
    BelieveItem,
  },
  data () {
    return {
      believes: this.$store.state.believes
    }
  }
}
</script>

<style scoped>

.believe-bg {
  background: #A85846;
}

.believe-wrapper {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 24px;
  padding-right: 24px;
}

.believe-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 72px 110px;
  position: relative;
  margin-top: 72px;
}

h2 {
  text-transform: uppercase;
}

@media (max-width: 950px) {
  .believe-container {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}

</style>
