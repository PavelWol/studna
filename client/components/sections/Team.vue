<template>
  <div class="team-bg">
    <div class="team-wrapper">
      <h2>Náš tým</h2>
      <div class="team-container">
        <TeamItem v-for="item in teams" :key="item.name" :image="require('/assets/images/' + item.image)" :name="item.name" :position="item.position" />
      </div>
    </div>
    <div class="section-bg"></div>
  </div>
</template>

<script>
import TeamItem from '~/components/interactive/TeamItem'

export default {
  name: 'Team',
  components: {
    TeamItem,
  },
  data () {
    return {
      teams: this.$store.state.teams
    }
  }
}
</script>

<style scoped>

.team-bg {
  background: #112636;
  position: relative;
}

.section-bg {
  background: linear-gradient(180deg, rgba(168, 88, 70, 0) 0%, #A85846 100%);
  width: 100%;
  position: absolute;
  bottom: 0;
  height: 400px;
}

.team-wrapper {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 24px;
  padding-right: 24px;
}

.team-container {
  display: flex;
  justify-content: space-between;
  position: relative;
  z-index: 1;
}

h2 {
  text-transform: uppercase;
}

@media (max-width: 950px) {
  .team-container {
    flex-direction: column;
  }
}

</style>
