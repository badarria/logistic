<template>
  <section id="about">
    <div class="d-flex justify-content-center justify-content-md-start about">
      <img
        src="../assets/img/decorative-routes-thing-top-small-header.png"
        class="about-img--small"
      />
      <div
        class="about-wrap align-items-md-center d-flex flex-column flex-md-row "
      >
        <div class="d-flex flex-column about-content">
          <h1 class="about-content--title">
            Logistic management software development
          </h1>
          <p class="about-content--text">
            We solve transportation and stock management problems for Factories,
            Manufacturers, Carriers, Resellers, E-commerce and even more. Any
            issue can be solved with smart digitalization.
          </p>
          <button
            class="align-self-md-end about-content--btn btn"
            @click="showModal"
          >
            Request a free consultation
          </button>
        </div>
        <div class="about-img">
          <img src="../assets/img/decorative-routes-thing.png" />
        </div>
      </div>
      <transition name="fade" mode="out-in">
        <Modal v-if="isModalVisible" @close="closeModal" />
      </transition>
    </div>
  </section>
</template>

<script>
import Modal from './modal'
export default {
  name: 'About',
  components: {
    Modal
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

section {
  width: 150vw;
  @include respond-to('sm') {
    width: 100vw;
  }
}

.about {
  padding: 168px 0 0 0;
  position: relative;
  @include respond-to('md') {
    padding: 114px 0 0 0;
  }

  &-wrap {
    transform: translateX(calc(50vw - 720px + 252px));

    @include respond-to('xl') {
      transform: translateX(252px);
    }
    @include respond-to('md') {
      transform: translateX(130px);
    }
    @include respond-to('sm') {
      transform: translateX(0px);
    }
  }

  &-img {
    width: 522px;
    min-width: 522px;

    @include respond-to('l') {
      transform: translateY(-15%);
    }
    @include respond-to('sm') {
      width: 363px;
      min-width: 363px;
      position: absolute;
      z-index: -1;
      bottom: 0;
      right: -158px;
    }
  }

  &-img--small {
    position: absolute;
    top: -116px;
    left: calc(50vw - 785px);

    @include respond-to('xl') {
      left: -105px;
    }
  }

  &-content {
    max-width: 710px;
    width: 55%;
    margin: 0 64px 0 0;
    @include respond-to('l') {
      max-width: 600px;
      margin: 0 32px 0 0;
    }
    @include respond-to('md') {
      max-width: 452px;
      margin: 0 0 0 0;
    }
    @include respond-to('sm') {
      width: 100%;
      padding: 0 25px 350px;
    }

    &--title {
      font-size: 55px;
      line-height: 55px;
      letter-spacing: -1.38px;
      font-family: $font-accent;
      text-transform: uppercase;

      @include respond-to('l') {
        font-size: 45px;
        line-height: 45px;
      }
      @include respond-to('md') {
        font-size: 35px;
        line-height: 35px;
      }
      @include respond-to('sm') {
        font-size: 30px;
        line-height: 30px;
      }
    }
    &--text {
      letter-spacing: -0.53px;
      font-size: 21px;
      opacity: 75%;
      width: 78%;
      max-height: 150px;
      overflow: hidden;
      margin: 50px 0 60px;

      @include respond-to('md') {
        font-size: 17px;
        width: 100%;
        margin: 68px 0 87px;
      }
      @include respond-to('sm') {
        font-size: 17px;
        margin: 50px 0 60px;
      }
    }
    &--btn {
      margin: 0 70px 0 0;

      @include respond-to('l') {
        margin: 0 10% 0 0;
      }
      @include respond-to('md') {
        margin: 0 7% 0 0;
      }
      @include respond-to('xs') {
        margin: 0 -10px 0;
      }
    }
  }
}
</style>
