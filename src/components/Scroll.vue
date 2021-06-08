<template>
  <div class="container">
    <div
      class="d-flex flex-column justify-content-center scroll align-items-center"
      @click="scrollTo"
    >
      <div class="scroll-icon">
        <img src="../assets/img/scroll-down-arrow.svg" alt="" />
      </div>
      <span class="scroll-text">Scroll for more information</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Scroll',
  methods: {
    scrollTo() {
      const header = document.querySelector('header')
      header.scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>

<style lang="scss" scoped>
.scroll {
  opacity: 50%;
  position: absolute;
  bottom: 10%;
  width: 50px;
  z-index: 10;
  transition: all 0.3s;

  &:hover {
    transition: all 0.3s;
    cursor: pointer;
    opacity: 100%;
  }
  &-text {
    font-weight: 300;
    font-size: 13px;
    letter-spacing: 0.16px;
    writing-mode: vertical-rl;
    transform: rotate(-180deg);
  }
  &-icon {
    margin: 0px 0 40px;
    transform: rotate(180deg);
  }
  @include respond-to('md') {
    display: none !important;
  }
}
</style>
