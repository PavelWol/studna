<template>
  <div class="map">
    <div class="panel">
      <img src="~/assets/images/3D_icon.png" alt="">
      <h3>
        STUDNA
        <br />
        <b>ŽIVÉ VODY</b>
      </h3>
      <p>
        Masarykova tř. 39
        <br />
        746 01 Opava
      </p>
    </div>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1143.4917453276037!2d17.902816931736062!3d49.936324256952425!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDnCsDU2JzEwLjEiTiAxN8KwNTQnMTMuMiJF!5e0!3m2!1scs!2scz!4v1632430535241!5m2!1scs!2scz" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
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
}

h3 {
  padding-left: 56px;
}

p {
  margin-top: 16px;
  padding-left: 56px;
}

iframe {
  width: 100%;
  height: 518px;
}

@media (max-width: 950px) {
  .map {
    flex-direction: column;
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
