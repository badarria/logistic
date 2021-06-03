<template>
  <div class="container">
    <div
      class="d-flex flex-column justify-content-center scroll align-items-center"
    >
      <span class="scroll-text">Scroll for more information</span>
      <div class="scroll-icon">
        <img src="../assets/img/scroll-down-arrow.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Scroll'
  //   methods: {
  //     scrollTo(refName) {
  //       const { offsetX, offsetY } = refName
  //       const elem = document.elementFromPoint(
  //         window.pageXOffset - offsetX,
  //         window.pageYOffset - offsetY
  //       )
  //       console.log(elem.getBoundingClientRect())

  //       console.log(offsetX, offsetY)
  //       console.log(elem)
  //       console.log(window.pageXOffset, window.pageYOffset)
  //     }
  //   }
}
</script>

<style lang="scss" scoped>
.scroll {
  opacity: 50%;
  position: fixed;
  height: 60vh;
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
    margin: 40px 0 0;
  }
}
</style>
