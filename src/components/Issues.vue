<template>
  <section class="container" id="issues">
    <div class="row flex-column issues align-items-center">
      <h3 class="issues-title">have you experienced any of these issues?</h3>
      <div class="glide carousel" id="issues-slider">
        <div class="glide__track" data-glide-el="track">
          <ul class="glide__slides">
            <li class="glide__slide carousel-slide">
              <p class="carousel-slide--title">
                Overwhelming and inaccurate paperwork
              </p>
              <p class="carousel-slide--text">
                Most documents, such as orders, invoices, contracts, etc. are
                stored in folders on endless shelves. They are never easy to
                find. Moreover, due to human factor, crucial mistakes take place
                that cost your company much time to solve, but also drain your
                budget.
              </p>
            </li>
            <li class="glide__slide carousel-slide">
              <p class="carousel-slide--title">
                Manual order management based on phone calls and emails
              </p>
              <p class="carousel-slide--text">
                Do your clients call you just to find out that the necessary
                product is currently out of stock? You waste resources by not
                providing them with actual information about your available
                inventory online
              </p>
            </li>
            <li class="glide__slide carousel-slide">
              <p class="carousel-slide--title">Inefficient truck load</p>
              <p class="carousel-slide--text">
                Without dynamic truck load scheduling, your company misses up to
                50% of the potential loading capability
              </p>
            </li>
          </ul>
        </div>
        <div
          class="d-flex align-items-center justify-content-between carousel-nav"
        >
          <div data-glide-el="controls" class="d-flex">
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
            <div
              data-glide-dir=">"
              class="controls--btn d-flex justify-content-center align-items-center"
            >
              <img src="../assets/img/arrow-right.png" alt="" />
            </div>
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
        </div>
      </div>
      <div class="issues-footer d-flex justify-content-center">
        <p class="issues-footer--text">
          Expenses reduction after implementing logistics management software!
        </p>
        <span class="issues-footer--nums">49,2%</span>
      </div>
    </div>
  </section>
</template>

<script>
import Glide from '@glidejs/glide'

export default {
  name: 'Issues',
  mounted() {
    new Glide('#issues-slider', {
      type: 'carousel',
      startAt: 0,
      perView: 3,
      gap: 15,
      startAts: 0
    }).mount()
  }
}
</script>

<style lang="scss" scoped>
.issues {
  margin: 12% 0 0;

  &-title {
    font-size: 35px;
    letter-spacing: -0.88px;
    font-family: $font-accent;
    text-transform: uppercase;
  }
  &-footer {
    margin: 13% 0 0;
    width: 100%;

    &--text {
      width: 340px;
      font-size: 25px;
      letter-spacing: -0.63px;
      opacity: 75%;
    }
    &--nums {
      font-family: $font-accent;
      font-size: 123px;
      line-height: 0.9;
    }
  }
}

.carousel {
  transform: translateX(7.5%);
  margin: 12% 0 0;
  width: 90%;
  max-width: 1290px;

  &-nav {
    width: 40.5%;
  }
  & .bullets {
    margin: 0 0 0 50px;
  }
  &-slide {
    height: 368px;
    background: $color-base;
    color: $color-white;
    padding: 68px 38px;
    max-width: 420px !important;

    &--title {
      font-size: 21px;
      font-weight: 700;
      line-height: 25px;
      letter-spacing: -0.53px;
    }
    &--text {
      font-size: 17px;
      letter-spacing: -0.43px;
      margin: 22px 0 0;
    }
  }
}
</style>
