<template>
  <div class="events-item">
    <img :src="image" alt="">
    <a v-if="href" :href="href">{{ heading }}</a>
    <h3 v-else>{{ heading }}</h3>
    <p>{{ description }}</p>
    <p class="place-time" v-html="adress"></p>
    <span v-if="subText" class="sub-text">{{ subText }}</span>
  </div>
</template>

<script>
export default {
  name: 'EventsItem',
  props: ['image', 'href', 'heading', 'description', 'adress', 'subText']
}
</script>

<style scoped>

.events-item {
  border-right: 1px solid rgba(255, 255, 255, 0.08);
  padding: 0 68px;
}

.events-item:first-child {
  padding-left: 0;
  height: 535px;
}

.events-item:last-child {
  padding-right: 0;
  border-right: none;
  margin-top: 285px;
}

.events-item:nth-child(2) {
  margin-top: 140px;
}

img {
  width: 36px;
}

h3, a {
  font-family: Bebas Neue, sans-serif;
  font-size: 40px;
  margin-top: 24px;
  text-transform: uppercase;
  color: #638C9F;
  display: block;
}

p {
  margin-top: 24px;
  line-height: 32px;
  color: rgba(255, 255, 255, .8);
}

p:not(.place-time) {
  max-width: 280px;
}

.place-time {
  margin-top: 72px;
  font-size: 16px;
  color: #ffffff;
}

span {
  font-family: Marcellus, sans-serif;
  font-size: 16px;
  line-height: 29px;
  color: rgba(255, 255, 255, .8);
  display: block;
  max-width: 190px;
  margin-left: 24px;
}

@media (max-width: 950px) {
  .events-item {
    border-right: none;
    border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    padding-left: 0 !important;
    padding-right: 0 !important;
    padding-bottom: 32px;
    padding-top: 32px;
    height: inherit !important;
    margin-top: 0 !important;
  }

  .events-item:last-child {
    border-bottom: none;
  }

  .place-time {
    margin-top: 32px;
  }

  p {
    max-width: unset !important;
  }
}

</style>
