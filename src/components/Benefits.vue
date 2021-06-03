<template>
  <section class="container" id="benefits">
    <div class="benefits d-flex align-items-center">
      <h2 class="benefits--title">
        how can you benefit from custom logistics software?
      </h2>
      <div class="d-flex flex-wrap points">
        <div class="points-row points-row--1 d-flex">
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
        </div>
        <div class="points-row points-row--2 d-flex">
          <div class="points-item">
            <div
              class="points-item--orange d-flex flex-column justify-content-center align-items-center"
            >
              <span>1</span>
            </div>
            <div class="points-item--content">
              <p class="points-item--title">Customized to your needs</p>
              <p class="points-item--text">
                A software is developed exclusively with your needs and plans in
                mind. This enables to solve unique problems efficiently
              </p>
            </div>
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div
              class="points-item--orange d-flex flex-column justify-content-center align-items-center"
            >
              <span>2</span>
            </div>
            <div class="points-item--content">
              <p class="points-item--title">Short-term ROI</p>
              <p class="points-item--text">
                You will experience the first returns right in the first month
                after integrating the system in your current processes
              </p>
            </div>
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
        </div>
        <div class="points-row points-row--3 d-flex">
          <div class="points-item">
            <div
              class="points-item--orange d-flex flex-column justify-content-center align-items-center"
            >
              <span>3</span>
            </div>
            <div class="points-item--content">
              <p class="points-item--title">Predictable scalability</p>
              <p class="points-item--text">
                A custom system grows along with your business since your
                company goals are taken into account in the development process
              </p>
            </div>
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div
              class="points-item--orange d-flex flex-column justify-content-center align-items-center"
            >
              <span>4</span>
            </div>
            <div class="points-item--content">
              <p class="points-item--title">Improve, not rebuild</p>
              <p class="points-item--text">
                Custom software supports and improves your running processes
                step-by-step. Your current system keeps working
              </p>
            </div>
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
          <div class="points-item">
            <div class="points-item--circle points-item--circle__first"></div>
            <div class="points-item--circle points-item--circle__second"></div>
            <div class="points-item--circle points-item--circle__third"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="consultation d-flex flex-column align-items-center">
      <div class="consultation-btn">
        <h3 class="consultation-btn--title">
          your business case is completely different?
          <span class="consultation-btn--title__accent">let's discuss</span>
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
import Modal from './Modal'
export default {
  name: 'Benefits',
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

.consultation {
  margin: 60px 0 0;

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
    }
    &--btn {
      width: 100%;
      margin: 30px 0 0;
    }
  }
}

.benefits {
  margin: 19% 0 0 5%;
  position: relative;

  &--title {
    position: absolute;
    top: 85px;
    left: 10%;
    z-index: 10;
    font-size: 35px;
    letter-spacing: -0.88px;
    line-height: 35px;
    text-transform: uppercase;
    font-family: $font-accent;
    width: 600px;
  }
}
.points {
  &-row--2,
  &-row--3 {
    margin: -82px 0 0;
  }

  &-item {
    margin: 0 -79px 0px 0;
    border-radius: 300px;
    width: 256px;
    height: 256px;
    position: relative;

    &--circle {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      border-radius: 300px;
      box-shadow: 0 0 0 16px rgb(241, 241, 241);
      transition: all 0.4s ease-out 0.2s;

      .points-item:hover & {
        transition: all 0.4s ease-out 0.2s;
        opacity: 0;
        // cursor:
      }
      &__first {
        width: 96px;
        height: 96px;
        transition: all 0.4s ease-out 0.2s;
        .points-item:hover & {
          width: 80px;
          height: 80px;
          transition: all 0.4s ease-out 0.2s;
        }
      }
      &__second {
        width: 158px;
        height: 158px;
        transition: all 0.6s ease-out 0.2s;

        .points-item:hover & {
          width: 112px;
          height: 112px;
          transition: all 0.4s ease-out 0.2s;
        }
      }
      &__third {
        width: 216px;
        height: 216px;
        transition: all 0.8s ease-out 0.2s;

        .points-item:hover & {
          width: 142px;
          height: 142px;
          transition: all 0.4s ease-out 0.2s;
        }
      }
    }
    &--content {
      position: absolute;
      z-index: 5;
      top: 50%;
      left: 50%;
      transform: translate(70px, -50%);
      width: 345px;
    }
    &--title {
      font-size: 25px;
      letter-spacing: -0.63px;
      font-family: $font-accent;
    }
    &--text {
      margin: 20px 0 0;
      font-size: 17px;
      letter-spacing: -0.43px;
      opacity: 75%;
    }
    &--orange {
      background: $color-pale-orange;
      width: 80px;
      height: 80px;
      position: absolute;
      z-index: 5;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      border-radius: 50px;
      color: $color-white;
      font-family: $font-accent;
      font-size: 19px;
      position: relative;
    }
  }
}
</style>
