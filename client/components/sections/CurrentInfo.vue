<template>
  <div class="info-bg">
    <div class="info">
      <h3>Aktuální <br /> informace</h3>
      <svg class="arrow" width="265" height="12" viewBox="0 0 265 12" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M1 6L258 6.00002" stroke="#5B2215" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="square" stroke-linejoin="round"/>
        <path d="M258 0L265 6L258 12V0Z" fill="#5B2215"/>
      </svg>
      <div class="next-events">
        <div>
          <h4>příští bohoslužba</h4>
          <p>
            📅 vždy v neděli <br />
            🕒 9:30 - 11:00
          </p>
        </div>
        <div class="seminar">
          <h4>Aktuálně není žádný seminář</h4>
          <p>
            📅 / <br />
            🕒 /
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
  padding-left: 24px;
  padding-right: 24px;
}

.arrow {
  align-self: center;
}

h3 {
  font-weight: bold;
  font-size: 40px;
  text-transform: uppercase;
  color: #5B2215;
}

h4, a {
  font-family: Bebas Neue, sans-serif;
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

.seminar {
  max-width: 164px;
}

.next-events {
  display: flex;
  justify-content: space-between;
}

.next-events div:not(:last-child) {
  margin-right: 64px;
}

@media (max-width: 950px) {
  .info {
    flex-direction: column;
  }

  .arrow {
    display: none;
  }

  a {
    font-size: 18px !important;
  }

  h3 {
    text-align: center;
  }

  h3 br {
    display: none;
  }

  p {
    font-size: 14px;
  }

  .next-events {
    margin-top: 24px;
    flex-direction: column;
  }

  .next-events div:not(:last-child) {
    margin-right: 0;
    margin-bottom: 16px;
  }
}

@media (min-width: 950px) {
  .mobile-line {
    display: none;
  }
}

</style>
