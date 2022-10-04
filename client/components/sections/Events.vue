<template>
  <div class="events-bg">
    <div class="events-wrapper">
      <EventsItem v-for="item in events" :key="item.heading" :image="require('/assets/images/' + item.image)" :href="item.href" :heading="item.heading" :description="item.description" :adress="item.adress" :subText="item.subText" :subsubText="item.subsubText" />
    </div>
  </div>
</template>

<script>
import EventsItem from '~/components/interactive/EventsItem'

export default {
  name: 'Events',
  components: {
    EventsItem,
  },
  data () {
    return {
      events: this.$store.state.events
    }
  }
}
</script>

<style>

.events-bg {
  background: #112636;
}

.events-wrapper {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: space-between;
  position: relative;
  padding-left: 24px;
  padding-right: 24px;
}

@media (max-width: 950px) {
  .events-wrapper {
    flex-direction: column;
  }
}

</style>
