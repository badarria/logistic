<template>
  <section class="d-flex justify-content-end" id="advantages">
    <div class="d-flex wrap">
      <div class="box">
        <h3 class="box--title">our advantages</h3>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">System Integration</p>
            <p>
              We help you with educating employees and integrating software in
              your running processes
            </p>
          </div>
        </div>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">Technical support</p>
            <p>
              We guarantee support and product maintenance after release and
              keep improving the system in cooperation with your team
            </p>
          </div>
        </div>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">Data security</p>
            <p>
              Your data is stored on secure servers based in Germany (or any
              other country on your request)
            </p>
          </div>
        </div>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">We speak your language</p>
            <p>
              Our managers are German- and English-speaking, so the business
              communication is clear and easy
            </p>
          </div>
        </div>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">Representative in Germany</p>
            <p>
              Our business analyst is based in Frankfurt am Main. Discussing all
              the business issues in person is much more efficient
            </p>
          </div>
        </div>
        <div class="box-item d-flex">
          <div class="box-item--point"></div>
          <div class="box-item--content">
            <p class="box-item--title">5 years experience in logistics</p>
            <p>
              We’ve successfully implemented custom
              logistics/transportation/stock and order management systems
            </p>
          </div>
        </div>
      </div>
      <div class="box box__left">
        <div class="box-wrap d-flex flex-column">
          <p class="box--text">
            Flawless communication with the Clockwise Software team resulted in
            a fleet management system that exactly met the needs of the
            municipal waste transportation company. The software runs on Android
            smartphones, so there was no need for expensive equipment, and the
            learning curve was low. We’ve implemented multi-tenancy to use this
            software in other projects connected with logistics.
          </p>
          <div class="box-author d-flex align-self-end ">
            <div class="box-author--info">
              <p class="box-author--name">
                Dan Weber
              </p>
              <p>CEO/CTO at Marketsoup</p>
            </div>
            <img
              src="../assets/img/author-1.png"
              alt=""
              class="box-author--img"
            />
          </div>
        </div>
        <div class="box-wrap d-flex flex-column">
          <p class="box--text">
            With the automatic load scheduling and proper route planning, we are
            finally able to use 100% of our truck load capacity. Also, order
            management and delivery have become much more efficient due to
            custom modules. In the first year, we have covered our investment in
            custom ERP system development
          </p>
          <div class="box-author d-flex align-self-end ">
            <div class="box-author--info">
              <p class="box-author--name">Vadim Chabanenko</p>
              <p>Director at UDK Gazbeton</p>
            </div>
            <img
              src="../assets/img/author-2.png"
              alt=""
              class="box-author--img"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default { name: 'Advantages' }
</script>

<style lang="scss" scoped>
.wrap {
  margin: 168px 0 0px 0px;
  width: 77%;
}
.box {
  width: 45%;
  max-width: 505px;
  margin: 0 54px 0px 0;
  padding: 0 0 40px 0;
  &__left {
    width: 55%;
    max-width: 633px;
    margin: 0 0px 0 54px;
    padding: 20px 40px;
    box-shadow: 0 10px 30px 0 rgba(0, 0, 0, 0.1);
    background: linear-gradient(140deg, #ffffff, #efefef);
  }
  &--title {
    font-size: 35px;
    letter-spacing: -0.88px;
    line-height: 35px;
    font-family: $font-accent;
    text-transform: uppercase;
    margin: 0 0 50px 0;
  }
  &-wrap {
    width: 75%;
    margin: 70px 0 0;
  }
  &--text {
    font-weight: 600;
    letter-spacing: -0.43px;
    font-size: 17px;
  }
  &-author {
    margin: 15px 0 0;
    &--info {
      text-align: right;
      margin: 0 15px 0 0;
      letter-spacing: -0.43px;
      font-size: 15px;
    }
    &--name {
      font-size: 17px;
      font-weight: 700;
    }
    &--img {
      filter: grayscale(100%);
    }
  }
  &-item {
    margin: 24px 0 0;
    &--point {
      width: 34px;
      height: 34px;
      background: $color-watermelon;
      border-radius: 50px;
    }
    &--title {
      font-size: 21px;
      letter-spacing: -0.53px;
      font-family: $font-accent;
    }
    &--content {
      width: 80%;
      margin: 0 0 0 32px;
    }
  }
}
</style>
