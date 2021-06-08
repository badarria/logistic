<template>
  <footer class="footer">
    <div class="container ">
      <div class=" d-flex justify-content-center justify-content-sm-start">
        <div
          class="footer-wrap d-flex flex-column justify-content-center justify-content-sm-around align-items-sm-center flex-sm-row "
        >
          <p>Data Protection / Imprint</p>
          <div class="footer-logo d-flex align-items-center">
            <img src="../assets/img/logo.png" alt="" class="footer-logo--img" />
            <div class="footer-logo--content">
              <p class="footer-logo--title">clockwise</p>
              <p>Software</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default { name: 'Footer' }
</script>

<style lang="scss" scoped>
.footer {
  background: $color-black;
  color: $color-white;
  font-weight: 600;
  letter-spacing: 0.12px;
  height: 104px;
  @include respond-to('xs') {
    height: 208px;
  }
  &-wrap {
    height: 104px;
    width: 100%;
    @include respond-to('xs') {
      height: 208px;
      width: auto;
    }
  }

  &-logo {
    @include respond-to('xs') {
      padding: 36px 0 0;
    }
    &--img {
      width: 24px;
      height: 24px;
      filter: grayscale(100%) brightness(5);
      margin: 0 15px 0 0;
    }
    &--content {
      font-size: 8px;
      letter-spacing: 0.07px;
      font-weight: 500;
    }
    &--title {
      font-family: $font-accent;
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.08px;
    }
  }
}
</style>
