<template>
  <header class="header">
    <div class="container">
      <div
        class="header-wrap d-flex justify-content-between align-items-center"
      >
        <div class="d-flex align-items-center header-logo">
          <div class="header-logo--img">
            <img src="../../assets/img/logo.png" />
          </div>
          <div class="d-flex flex-column header-logo--titlebox">
            <span class="header-logo--title">Clockwise</span>
            <span>Software</span>
          </div>
        </div>

        <div class="burger">
          <Burger />
        </div>

        <nav class="nav d-flex ">
          <ul class="nav-wrap d-flex align-items-center justify-content-center">
            <li class="nav-item" @click="scrollTo('#benefits')">
              <link href="#benefits" class="nav-item--link" />Benefits
            </li>
            <li class="nav-item" @click="scrollTo('#advantages')">
              <link href="#advantages" class="nav-item--link" />Advantages
            </li>
            <li class="nav-item" @click="scrollTo('#achievments')">
              <link href="#achievments" class="nav-item--link" />Achievments
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
import Burger from './burger'

export default {
  name: 'Header',
  components: { Burger },
  methods: {
    scrollTo(name) {
      var element = document.querySelector(name)
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>

<style lang="scss" scoped>
.burger {
  display: none !important;
  @include respond-to('sm') {
    display: inherit !important;
  }
}

.header {
  width: 100%;
  z-index: 1;
  height: 144px;
  background: $color-white;

  &-wrap {
    padding: 40px 0px;
  }
  &-logo {
    &--img {
      width: 64px;
      height: 64px;
      margin: 0 16px 0 0;

      @include respond-to('md') {
        margin: 0 0px 0 38px;
      }
      @include respond-to('sm') {
        margin: 0 24px 0 22px;
      }
    }
    &--titlebox {
      line-height: 1;
      padding: 5px 0 0 0;

      @include respond-to('md') {
        display: none !important;
      }
      @include respond-to('sm') {
        display: inherit !important;
      }
    }
    &--title {
      font-family: $font-accent;
      text-transform: uppercase;
      font-size: 20px;
    }
  }

  &-langs {
    display: flex;
    width: 16%;

    @include respond-to('md') {
      width: 12%;
    }
    @include respond-to('sm') {
      display: none !important;
    }
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

.nav {
  padding: 0 16px 0;
  flex-grow: 1;
  @include respond-to('sm') {
    display: none !important;
  }

  &-wrap {
    width: 100%;
  }
  &-item {
    margin: 0 15% 0 0;
    font-weight: 600;
    font-size: 17px;
    letter-spacing: 0.13px;
    transition: all 0.3s;

    &:last-child {
      margin: 0;
    }
    &:hover {
      transition: all 0.3s;
      cursor: pointer;
      color: $color-watermelon;
    }
  }
}
</style>
