<template>
  <div class="description-bg">
    <div class="gradient"></div>
    <div class="description-wrapper">
      <div class="text">
        <p>
          Věříme v Boží moc a v Jeho zázraky, které se dějí i v dnešní době.
          Proto se věnujeme službě vnitřního uzdravení. Bůh přináší řešení do každé situace.
          Rádi se osobně setkáme s každým, kdo bude mít zájem.
        </p>
        <div class="img-container">
          <img class="signature" src="~/assets/images/eliasovi.svg" alt="">
        </div>
      </div>
      <img class="big-img" src="~/assets/images/description_img.png" alt="">
    </div>
    <div class="fake-bg"></div>
  </div>
</template>

<script>
  export default {
    name: 'Description',
  }
</script>

<style scoped>

.description-bg {
  background: #638C9F;
  position: relative;
}

.gradient {
  position: absolute;
  top: 0;
  width: 100%;
  background: linear-gradient(0deg, rgba(168, 88, 70, 0) 0%, #A85846 100%);
  height: 300px;
}

.description-wrapper {
  max-width: 1120px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: space-between;
  position: relative;
  z-index: 1;
  padding-left: 24px;
  padding-right: 24px;
}

.text {
  max-width: 475px;
}

p {
  font-size: 24px;
  color: rgba(255, 255, 255, 0.8);
  line-height: 43px;
}

.img-container {
  text-align: right;
  margin-right: 40px;
}

.big-img {
  max-width: 560px;
  margin-left: 80px;
}

.fake-bg {
  background: #112636;
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 125px;
}

@media (max-width: 950px) {
  .description-wrapper {
    flex-direction: column;
    align-items: center;
    max-width: 500px;
  }

  .big-img {
    width: 100%;
    margin-left: 0;
    margin-top: 44px;
  }

  .text {
    position: relative;
  }

  p {
    font-size: 18px;
    line-height: 32px;
  }

  .img-container {
    position: absolute;
    bottom: 0;
    right: 0;
    transform: translateY(100%);
    margin-right: 0;
  }

  .img-container img {
    width: 132px;
  }

  .fake-bg {
    height: 72px;
  }
}

</style>
