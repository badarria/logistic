<template>
  <section class="container" id="about">
    <div class="d-flex justify-content-between about">
      <img
        src="../assets/img/decorative-routes-thing-top-small-header.png"
        class="about-img--small"
      />
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
          class="align-self-end about-content--btn btn"
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
  </section>
</template>

<script>
import Modal from './Modal'
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
.about {
  padding: 10% 0 0 15%;
  position: relative;

  &-img {
    margin: 0 -115px 0 0;
    width: 522px;
  }
  &-img--small {
    position: absolute;
    top: -17%;
    left: -12%;
  }

  &-content {
    width: 60%;
    &--title {
      margin: 60px 0 0;
      font-size: 55px;
      line-height: 55px;
      letter-spacing: -1.38px;
      font-family: $font-accent;
      text-transform: uppercase;
    }
    &--text {
      letter-spacing: -0.53px;
      font-size: 21px;
      opacity: 75%;
      width: 78%;
      max-height: 150px;
      overflow: hidden;
      margin: 50px 0 60px;
    }
    &--btn {
      margin: 0 10% 0 0;
    }
  }
}
</style>
