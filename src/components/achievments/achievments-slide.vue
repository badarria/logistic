<template>
  <li
    class="glide__slide d-flex flex-column-reverse flex-md-row carousel-slide align-items-center align-content-center"
  >
    <div class="carousel-slide--img d-flex flex-column align-items-center">
      <img src="../../assets/img/achievment.png" alt="" />
      <span>double truck day load capacity increase</span>
    </div>
    <div class="carousel-slide--content d-flex flex-column">
      <p class="carousel-slide--title">
        ERP system for construction materials factory
      </p>
      <p>
        Custom logistics software includes several modules that enabled to fully
        digitalize a factory
      </p>
      <ul>
        <li>Order and stock management optimization</li>
        <li>Automatic invoicing and accounting</li>
        <li>Delivery scheduling and route planning</li>
        <li>Automatic contractors selection</li>
      </ul>

      <p>
        Eliminating manual work enabled the factory to double truck day load
        capacity (an increase from 45 to 92 trucks per day) and save over 60.000
        EUR in the first year.
      </p>
    </div>
  </li>
</template>

<script>
export default { name: 'AchievmentsSlide' }
</script>

<style lang="scss" scoped>
.carousel-slide {
  padding: 0 7.5px;
  &--img {
    width: 470px;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: -0.38px;
    text-align: center;
    margin: 0 16px 0 0;

    @include respond-to('md') {
      & img {
        width: 366px;
      }
    }
    @include respond-to('sm') {
      width: 100%;
      margin: 120px 0px 0;
      height: 600px;
    }
  }

  &--content {
    width: 40%;
    max-width: 345px;
    opacity: 75%;
    letter-spacing: -0.43px;
    padding: 0 7.5px;
    & p {
      margin: 10px 0 0;
    }
    & ul {
      padding: 0 0 0px 15px;
      & li {
        list-style-type: '– ';
      }
    }

    @include respond-to('md') {
      max-width: 500px;
      max-width: 600px;
    }
    @include respond-to('sm') {
      width: 100%;
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
</style>
