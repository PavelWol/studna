<template>
  <div class="info-bg">
    <div class="info">
      <h3>Aktuální <br /> informace</h3>
      <div class="next-events">
        <div>
          <h4>příští bohoslužba</h4>
          <p>
            📅 15. 8. 2021 <br />
            🕒 10:00 - 11:30
          </p>
        </div>
        <div>
          <h4>Seminář strach</h4>
          <p>
            📅 24. 11. 2021 <br />
            🕒 12:00 - 18:00
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'CurrentInfo',
}
</script>

<style scoped>

.info-bg {
  background: #A85846;
  padding: 56px 0;
}

.info {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: space-between;
}

h3 {
  font-weight: bold;
  font-size: 40px;
  text-transform: uppercase;
  color: #5B2215;
}

h4 {
  font-weight: bold;
  font-size: 24px;
  line-height: 104%;
  text-transform: uppercase;
  color: #5B2215;
}

p {
  font-size: 16px;
  line-height: 180%;
  color: #FFFFFF;
  margin-top: 8px;
}

.next-events {
  display: flex;
  justify-content: space-between;
}

.next-events div:first-child {
  margin-right: 112px;
}

</style>
