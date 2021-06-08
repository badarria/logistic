<template>
  <div class="d-flex flex-column">
    <div class="menu-icon" v-bind:class="{ open: isOpen }" @click="changeOpen">
      <span class="menu-icon--line"></span>
      <span class="menu-icon--line"></span>
      <span class="menu-icon--line"></span>
    </div>

    <div
      v-bind:class="{ open: isOpen }"
      class="menu--hidden d-flex flex-column justify-content-end"
    >
      <div
        v-bind:class="{ open: isOpen }"
        class="menu d-flex flex-column justify-content-end"
      >
        <nav class="menu--wrap d-flex flex-column ">
          <ul class="menu--list d-flex flex-column">
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

        <div class="langs d-flex justify-content-between">
          <p class="langs--title">Language</p>
          <div class="langs-btns">
            <button class="langs-btns--item">de</button>
            <button class="langs-btns--item selected">en</button>
          </div>
        </div>
        <button class="btn menu--btn" @click="showModal">
          Request a free consultation
        </button>
      </div>
    </div>
    <Modal v-if="isModalVisible" @close="closeModal" />
  </div>
</template>

<script>
import Modal from '../modal'

export default {
  name: 'Burger',
  components: { Modal },
  data() {
    return {
      isOpen: false,
      isModalVisible: false
    }
  },
  methods: {
    scrollTo(name) {
      var element = document.querySelector(name)
      this.changeOpen()

      element.scrollIntoView({ behavior: 'smooth' })
    },
    changeOpen() {
      const body = document.querySelector('body')
      this.isOpen = !this.isOpen

      if (this.isOpen === true) {
        body.classList.add('open')
      } else {
        body.classList.remove('open')
      }
    },
    showModal() {
      this.changeOpen()
      this.isModalVisible = true
    },
    closeModal() {
      this.isModalVisible = false
    }
  }
}
</script>

<style lang="scss" scoped>
.menu-icon {
  padding: 16px;

  &--line {
    display: block;
    width: 18px;
    height: 3px;
    border-radius: 5px;
    background: $color-black;
    margin: 3px 0 0;
    transition: all 0.3s;

    .menu-icon.open &:last-child {
      margin: 0;
    }
    .menu-icon.open & {
      transition: all 0.3s;
      transform: rotate(-45deg);
    }
    .menu-icon.open &:first-child {
      transform: rotate(45deg) translate(4.5px, 4px);
    }
    .menu-icon.open &:last-child {
      display: none !important;
    }
  }
}

.menu {
  overflow: hidden;
  display: none !important;
  height: 100vh;
  &--hidden {
    position: absolute;
    top: 140px;
    left: 0;
    right: 0;
    background: $color-white;
    z-index: 50;
    opacity: 0;
    transition: all 0.3s;

    &.open {
      transition: all 0.3s;
      opacity: 1;
    }
  }

  &.open {
    display: inherit !important;
  }
  &--list,
  &--wrap,
  .langs {
    width: 100%;
  }

  &-item,
  .langs {
    box-sizing: border-box;
    padding: 10px 40px;
    box-shadow: inset 0 1px 0 #f3f3f3, inset 0 -1px 0 #f3f3f3;
    font-weight: 600;
    font-size: 21px;
    letter-spacing: -0.53px;
    transition: all 0.3s;
  }
  .langs {
    margin: 50px 0 0;
  }
  &-item:last-child {
    margin: 0;
  }
  &-item:hover {
    transition: all 0.3s;
    cursor: pointer;
    color: $color-watermelon;
  }
  &--btn {
    margin: 50px 15px 55px;
    padding: 5px 42px;
  }
}

.langs {
  &-btns--item {
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
</style>
