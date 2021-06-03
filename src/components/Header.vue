<template>
  <header class="header">
    <div class="container">
      <div class="row justify-content-between align-items-center">
        <div
          class="row justify-content-between  align-items-center header-logo"
        >
          <div class="header-logo--img">
            <img src="../assets/img/logo.png" />
          </div>
          <div class="row flex-column header-logo--titlebox">
            <span class="header-logo--title">Clockwise</span>
            <span>Software</span>
          </div>
        </div>
        <nav class="menu">
          <ul class="row align-items-center">
            <li class="menu-item" @click="scrollTo('#benefits')">
              <link href="#benefits" class="menu-item--link" />Benefits
            </li>
            <li class="menu-item" @click="scrollTo('#advantages')">
              <link href="#advantages" class="menu-item--link" />Advantages
            </li>
            <li class="menu-item" @click="scrollTo('#achievments')">
              <link href="#achievments" class="menu-item--link" />Achievments
            </li>
          </ul>
        </nav>
        <div class="header-langs">
          <button class="header-langs--btn">de</button>
          <button class="header-langs--btn selected">en</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    scrollTo(name) {
      var element = document.querySelector(name)
      console.log(element)
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  height: 144px;
  background: $color-white;
  padding: 40px 54px;

  &-logo {
    width: 204px;
    &--img {
      width: 64px;
      height: 64px;
      margin: 0 16px 0 0;
    }
    &--titlebox {
      line-height: 1;
      padding: 5px 0 0 0;
    }
    &--title {
      font-family: $font-accent;
      text-transform: uppercase;
      font-size: 20px;
    }
  }

  &-langs {
    display: flex;
    width: 288px;
    &--btn {
      margin: 0 16px 0 0;
      font-weight: 600;
      font-size: 17px;
      letter-spacing: 0.13px;
      border: none;
      outline: none;
      background: none;
      color: $color-black;
      opacity: 25%;
      text-transform: uppercase;
      transition: all 0.3s;

      &.selected {
        opacity: 100%;
      }
      &:hover {
        cursor: pointer;
        transition: all 0.3s;
        opacity: 100%;
      }
    }
  }
}

.menu {
  padding: 0 16px 0;
  &-item {
    margin: 0 32px;
    font-weight: 600;
    font-size: 17px;
    letter-spacing: 0.13px;
    transition: all 0.3s;
    &:hover {
      transition: all 0.3s;
      cursor: pointer;
      color: $color-watermelon;
    }
  }
}
</style>
