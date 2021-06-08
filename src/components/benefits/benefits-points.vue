<template>
  <div class="benefits d-flex flex-column">
    <h2 class="benefits--title">
      how can you benefit from custom logistics software?
    </h2>
    <div class="d-flex flex-wrap flex-column flex-md-row points">
      <div
        class="d-flex points-row flex-column flex-md-row  flex-wrap points-row--first"
      >
        <div class="d-flex points-row--half">
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
        <div class="d-flex points-row--half">
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
      </div>
      <div
        class="d-flex points-row flex-column flex-md-row  flex-wrap points-row--second"
      >
        <div class="d-flex points-row--half">
          <div class="points-item">
            <div
              class="points-item--orange points-item--inner d-flex flex-column justify-content-center align-items-center"
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
          </div>

          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
        <div class="d-flex points-row--half">
          <div class="points-item">
            <div
              class="points-item--orange points-item--inner d-flex flex-column justify-content-center align-items-center"
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
          </div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
      </div>

      <div
        class="d-flex flex-column flex-md-row  points-row flex-wrap points-row--third"
      >
        <div class="d-flex points-row--half">
          <div class="points-item">
            <div
              class="points-item--orange points-item--inner d-flex flex-column justify-content-center align-items-center"
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
          </div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
        <div class="d-flex points-row--half">
          <div class="points-item">
            <div
              class="points-item--orange points-item--inner d-flex flex-column justify-content-center align-items-center"
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
          </div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
      </div>
      <div
        class="d-flex flex-column flex-md-row  points-row flex-wrap points-row--fourth"
      >
        <div class="d-flex points-row--half">
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
          <div class="points-item"><div class="points-item--inner"></div></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BenefitsPoints'
}
</script>

<style lang="scss" scoped>
%centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.benefits {
  margin: 19% 0 0 5%;
  position: relative;

  @include respond-to('l') {
    margin: 25% 0 0 5%;
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

    @include respond-to('l') {
      position: static;
    }

    @include respond-to('md') {
      font-size: 25px;
      line-height: 25px;
      padding: 0 78px 0;
    }
  }
}
.points {
  &-item {
    border-radius: 50%;
    width: 172px;
    height: 172px;
    position: relative;

    &::before,
    &::after,
    &--inner::before {
      content: '';
      @extend %centered;
      border-radius: 50%;
      box-shadow: 0 0 0 16px rgb(241, 241, 241);
      transition: all 0.4s ease-out 0.2s;
    }
    &::before {
      width: 158px;
      height: 158px;
    }
    &::after {
      width: 216px;
      height: 216px;
    }
    &--inner {
      @extend %centered;
      &::before {
        width: 96px;
        height: 96px;
      }
    }

    &:hover .points-item--inner::before {
      width: 80px;
      height: 80px;
      transition: all 0.4s ease-out 0.2s;
      opacity: 0;
    }
    &:hover.points-item::before {
      width: 112px;
      height: 112px;
      transition: all 0.3s ease-out 0.1s;
      opacity: 0;
    }
    &:hover.points-item::after {
      width: 142px;
      height: 142px;
      transition: all 0.3s ease-out 0.1s;
      opacity: 0;
    }

    &--content {
      position: absolute;
      z-index: 5;
      top: 50%;
      left: 50%;
      transform: translate(70px, -50%);
      width: 345px;

      @include respond-to('xs') {
        width: 220px;
      }
    }
    &--title {
      font-size: 25px;
      line-height: 25px;
      letter-spacing: -0.63px;
      font-family: $font-accent;
      @include respond-to('xs') {
        text-transform: uppercase;
        font-size: 21px;
        line-height: 21px;
      }
    }
    &--text {
      margin: 20px 0 0;
      font-size: 17px;
      letter-spacing: -0.43px;
      opacity: 75%;

      @include respond-to('xs') {
        font-size: 15px;
        line-height: 15px;
        letter-spacing: -0.38px;
        padding: 0 30px 0 0;
      }
    }
    &--orange {
      background: $color-pale-orange;
      width: 80px;
      height: 80px;
      border-radius: 50%;
      z-index: 5;
      color: $color-white;
      font-family: $font-accent;
      font-size: 19px;
    }
  }

  &-row {
    & .points-item:nth-child(2),
    & .points-item:nth-child(3) {
      @include respond-to('xs') {
        display: none !important;
      }
    }
    &--first {
      @include respond-to('l') {
        display: none !important;
      }
    }
    &--second {
      @include respond-to('l') {
        margin: 80px 0 0;
      }
    }

    & div:nth-child(2) {
      & div:nth-child(3) {
        display: none !important;

        @include respond-to('l') {
          display: block !important;
        }

        @include respond-to('xs') {
          display: none !important;
        }
      }
    }

    &:last-child {
      display: none !important;
      @include respond-to('l') {
        display: block !important;
      }
    }
  }
}
</style>
