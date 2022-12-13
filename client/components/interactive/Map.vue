<template>
  <div class="map">
    <div class="panel">
        <img src="~/assets/images/3D_icon.png" alt="">
      <div class="map-text">
        <h3>
          STUDNA
          <br />
          <b>ŽIVÉ VODY</b>
        </h3>
        <p>
          Popská 3
          <br />
          746 01 Opava
        </p>
      </div>
    </div>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d970.70838208156!2d17.900746447265234!3d49.937354936951685!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4713d81362e6f559%3A0x4191feaeef267d5c!2sPopsk%C3%A1%203%2C%20746%2001%20Opava!5e0!3m2!1scs!2scz!4v1670918611954!5m2!1scs!2scz" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
  </div>
</template>

<script>

export default {
  namee: 'Map',
}

</script>

<style scoped>

.map {
  display: flex;
  justify-content: space-between;
}

.panel {
  background: #0C1F2E;
  padding-top: 24px;
  position: relative;
}

.map-text {
  position: absolute;
  bottom: 56px;
}

h3 {
  padding-left: 56px;
}

p {
  margin-top: 16px;
  padding-left: 56px;
  color: rgba(255, 255, 255, 0.8);
}

iframe {
  width: 100%;
  height: 518px;
}

@media (max-width: 950px) {
  .map {
    flex-direction: column;
  }

  .map-text {
    position: relative;
    bottom: 40px;
  }

  p:first-of-type {
    padding-bottom: unset;
  }

  .panel img {
    width: 100%;
  }

  h3, p {
    padding-left: 40px;
  }

  p {
    padding-bottom: 40px;
  }

  iframe {
    height: 240px;
  }
}

</style>
