<template>
  <section id="achievments">
    <Scroll />
    <div class="achievments d-flex flex-column align-items-center">
      <h3 class="achievments--title">
        what our partners have achieved with custom transpot management software
      </h3>
      <div class="box d-flex ">
        <img
          src="../../assets/img/decorative-routes-thing.png"
          alt=""
          class="box--img"
        />
        <div class="glide carousel " id="achievments-slider">
          <div
            data-glide-el="controls"
            class="d-flex justify-content-between align-items-center carousel-nav"
          >
            <div
              data-glide-dir="<"
              class="controls--btn d-flex justify-content-center align-items-center"
            >
              <img
                src="../../assets/img/arrow-right.png"
                alt=""
                class="controls--btn__prev"
              />
            </div>
            <div class="glide__bullets bullets" data-glide-el="controls[nav]">
              <button
                class="glide__bullet bullets--point"
                data-glide-dir="=0"
              ></button>
              <button
                class="glide__bullet bullets--point"
                data-glide-dir="=1"
              ></button>
              <button
                class="glide__bullet bullets--point"
                data-glide-dir="=2"
              ></button>
            </div>
            <div
              data-glide-dir=">"
              class="controls--btn d-flex justify-content-center align-items-center"
            >
              <img src="../../assets/img/arrow-right.png" alt="" />
            </div>
          </div>
          <div class="glide-track" data-glide-el="track">
            <ul class="glide__slides">
              <AchievmentsSlide />
              <AchievmentsSlide />
              <AchievmentsSlide />
            </ul>
          </div>
        </div>
      </div>
      <div class="footer">
        <p class="footer--text">
          discuss your project with the professionals
        </p>
        <button class="btn footer--btn" @click="showModal">
          Let's discuss
        </button>
      </div>
    </div>
    <transition name="fade" mode="out-in">
      <Modal v-if="isModalVisible" @close="closeModal" />
    </transition>
  </section>
</template>

<script>
import Glide from '@glidejs/glide'
import Modal from '../modal'
import AchievmentsSlide from './achievments-slide'
import Scroll from '../scroll'

export default {
  name: 'Achievments',
  mounted() {
    new Glide('#achievments-slider', {
      type: 'carousel',
      startAt: 0,
      perView: 1,
      gap: 15,
      startAts: 0,
      breakpoints: {
        768: {
          perView: 1
        }
      }
    }).mount()
  },
  components: {
    Modal,
    AchievmentsSlide,
    Scroll
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
#achievments {
  position: relative;
}

.achievments {
  margin: 20% 0 0;

  &--title {
    width: 55%;
    max-width: 710px;
    margin: 0 0 0 200px;
    font-family: $font-accent;
    font-size: 35px;
    line-height: 35px;
    padding: 16px;
    text-transform: uppercase;
    letter-spacing: -0.88px;
    text-align: right;

    @include respond-to('md') {
      font-size: 25px;
      line-height: 25px;
      letter-spacing: -0.63px;
      text-align: right;
      margin: 0 0 0;
      width: 100%;
    }
  }
}

.box {
  margin: 100px 20px 0;
  width: 65%;
  max-width: 912px;
  position: relative;

  &--img {
    position: absolute;
    top: 55%;
    left: -57%;
    width: 512px;
    z-index: 0;
    object-fit: contain;
    @include respond-to('l') {
      top: 55%;
      left: -43%;
    }

    @include respond-to('md') {
      top: auto;
      bottom: -44%;
      left: -168px;
      width: 363px;
    }
    @include respond-to('sm') {
      top: auto;
      bottom: 0;
    }
  }

  @include respond-to('l') {
    width: 100%;
  }
}

.carousel {
  overflow: hidden;

  &-nav {
    margin: 0 0 5px 20%;
    width: 38%;

    @include respond-to('md') {
      width: 330px;
      margin: 0 0 0 60px;
    }

    @include respond-to('sm') {
      width: 100%;
      margin: 0 0 0;
      position: absolute;
      bottom: 620px;
      z-index: 100;
    }
  }
}

.footer {
  margin: 10% 0 12%;
  max-width: 345px;
  @include respond-to('md') {
    margin: 100px 0 205px;
  }
  &--text {
    text-transform: uppercase;
    text-align: center;
    font-family: $font-accent;
    font-size: 17px;
    letter-spacing: -0.43px;
  }
  &--btn {
    margin: 45px 0 0 0;
    width: 100%;
  }
}
</style>
