<template>
  <section class="container" id="achievments">
    <div class="achievments d-flex flex-column align-items-center">
      <h3 class="achievments--title">
        what our partners have achieved with custom transpot management software
      </h3>
      <div class="box d-flex">
        <img
          src="../assets/img/decorative-routes-thing.png"
          alt=""
          class="box--img"
        />
        <div class="glide carousel" id="achievments-slider">
          <div
            data-glide-el="controls"
            class="d-flex justify-content-between align-items-center carousel-nav"
          >
            <div
              data-glide-dir="<"
              class="controls--btn d-flex justify-content-center align-items-center"
            >
              <img
                src="../assets/img/arrow-right.png"
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
              <img src="../assets/img/arrow-right.png" alt="" />
            </div>
          </div>
          <div class="glide-track" data-glide-el="track">
            <ul class="glide__slides">
              <li
                class="glide__slide d-flex justify-content-between carousel-slide"
              >
                <div class="carousel-slide--img">
                  <img src="../assets/img/achievment.png" alt="" />
                  <span>double truck day load capacity increase</span>
                </div>
                <div class="carousel-slide--content d-flex flex-column">
                  <p class="carousel-slide--title">
                    ERP system for construction materials factory
                  </p>
                  <p>
                    Custom logistics software includes several modules that
                    enabled to fully digitalize a factory
                  </p>
                  <ul>
                    <li>Order and stock management optimization</li>
                    <li>Automatic invoicing and accounting</li>
                    <li>Delivery scheduling and route planning</li>
                    <li>Automatic contractors selection</li>
                  </ul>

                  <p>
                    Eliminating manual work enabled the factory to double truck
                    day load capacity (an increase from 45 to 92 trucks per day)
                    and save over 60.000 EUR in the first year.
                  </p>
                </div>
              </li>
              <li
                class="glide__slide d-flex justify-content-between carousel-slide"
              >
                <div class="carousel-slide--img">
                  <img src="../assets/img/achievment.png" alt="" />
                  <span>double truck day load capacity increase</span>
                </div>
                <div class="carousel-slide--content  d-flex flex-column">
                  <p class="carousel-slide--title">
                    ERP system for construction materials factory
                  </p>
                  <p>
                    Custom logistics software includes several modules that
                    enabled to fully digitalize a factory
                  </p>
                  <ul>
                    <li>Order and stock management optimization</li>
                    <li>Automatic invoicing and accounting</li>
                    <li>Delivery scheduling and route planning</li>
                    <li>Automatic contractors selection</li>
                  </ul>

                  <p>
                    Eliminating manual work enabled the factory to double truck
                    day load capacity (an increase from 45 to 92 trucks per day)
                    and save over 60.000 EUR in the first year.
                  </p>
                </div>
              </li>
              <li
                class="glide__slide d-flex justify-content-between carousel-slide"
              >
                <div class="carousel-slide--img">
                  <img src="../assets/img/achievment.png" alt="" />
                  <span>double truck day load capacity increase</span>
                </div>
                <div class="carousel-slide--content  d-flex flex-column">
                  <p class="carousel-slide--title">
                    ERP system for construction materials factory
                  </p>
                  <p>
                    Custom logistics software includes several modules that
                    enabled to fully digitalize a factory
                  </p>
                  <ul>
                    <li>Order and stock management optimization</li>
                    <li>Automatic invoicing and accounting</li>
                    <li>Delivery scheduling and route planning</li>
                    <li>Automatic contractors selection</li>
                  </ul>

                  <p>
                    Eliminating manual work enabled the factory to double truck
                    day load capacity (an increase from 45 to 92 trucks per day)
                    and save over 60.000 EUR in the first year.
                  </p>
                </div>
              </li>
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
import Modal from './Modal'

export default {
  name: 'Achievments',
  mounted() {
    new Glide('#achievments-slider', {
      type: 'carousel',
      startAt: 0,
      perView: 1,
      gap: 15,
      startAts: 0
    }).mount()
  },
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
.achievments {
  margin: 20% 0 18%;

  &--title {
    width: 55%;
    max-width: 710px;
    font-family: $font-accent;
    font-size: 35px;
    text-transform: uppercase;
    line-height: 35px;
    letter-spacing: -0.88px;
    text-align: right;
  }
}

.box {
  margin: 100px 0 0;
  width: 65%;
  position: relative;
  &--img {
    position: absolute;
    top: 55%;
    left: -55%;
    max-width: 512px;
    width: 60%;
    object-fit: contain;
  }
}

.carousel {
  overflow: hidden;
  &-slide {
    &--img {
      width: 50%;
      max-width: 470px;
      text-transform: uppercase;
      font-weight: 700;
      letter-spacing: -0.38px;
      text-align: center;
    }
    &--content {
      width: 40%;
      max-width: 345px;
      opacity: 75%;
      letter-spacing: -0.43px;
      & p {
        margin: 10px 0 0;
      }
      & ul {
        padding: 0 0 0px 15px;
        & li {
          list-style-type: '– ';
        }
      }
    }

    &--title {
      font-family: $font-accent;
      line-height: 30px;
      letter-spacing: -0.63px;
      font-size: 25px;
      opacity: 100%;
    }
  }
  &-nav {
    margin: 0 0 5px 20%;
    width: 38%;
  }
}

.footer {
  margin: 10% 0 0;
  max-width: 345px;
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
