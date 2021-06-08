<template>
  <section class="container" id="benefits">
    <BenifitsPoints />
    <div class="consultation d-flex flex-column align-items-center">
      <div class="consultation-btn">
        <h3 class="consultation-btn--title">
          your business case is completely different?
          <br /><span class="consultation-btn--title__accent"
            >let's discuss</span
          >
        </h3>
        <button class="consultation-btn--btn btn" @click="showModal">
          Fill in the contact form
        </button>
      </div>
    </div>
    <transition name="fade" mode="out-in">
      <Modal v-if="isModalVisible" @close="closeModal" />
    </transition>
  </section>
</template>

<script>
import Modal from '../modal'
import BenifitsPoints from './benefits-points'

export default {
  name: 'Benefits',
  components: {
    Modal,
    BenifitsPoints
  },
  data() {
    return {
      isModalVisible: false
    }
  },
  methods: {
    showModal() {
      this.isModalVisible = true
    },
    closeModal() {
      this.isModalVisible = false
    }
  }
}
</script>

<style lang="scss" scoped>
.fade-enter-active {
  transition: all 0.3s ease;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.consultation {
  margin: 60px 0 0;
  @include respond-to('l') {
    position: relative;
    margin: 0;
    top: -44px;
  }

  &-btn {
    width: 345px;
    &--title {
      font-family: $font-accent;
      font-size: 25px;
      line-height: 30px;
      letter-spacing: -0.63px;
      text-transform: uppercase;
      text-align: center;
      &__accent {
        color: $color-watermelon;
      }
      @include respond-to('xs') {
        font-size: 21px;
        line-height: 21px;
        letter-spacing: -0.53px;
      }
    }
    &--btn {
      width: 100%;
      margin: 30px 0 0;
    }
  }
}

.benefits {
  margin: 19% 0 0 10%;
  position: relative;

  @include respond-to('md') {
    margin: 20% 0 0 0;
  }

  @include respond-to('xs') {
    margin: 20% 0 0 -5%;
  }

  &--title {
    position: absolute;
    top: 85px;
    left: 10%;
    z-index: 10;
    font-size: 35px;
    line-height: 35px;
    letter-spacing: -0.88px;
    text-transform: uppercase;
    font-family: $font-accent;
    width: 600px;
  }
}
</style>
