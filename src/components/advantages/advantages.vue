<template>
  <section
    class="d-flex justify-content-center justify-content-lg-end"
    id="advantages"
  >
    <div class="d-flex wrap flex-column flex-lg-row align-items-center">
      <div class="box">
        <h3 class="box--title">our advantages</h3>
        <AdvantagesListItem
          title="System Integration"
          description="We help you with educating employees and integrating software in
              your running processes"
        />
        <AdvantagesListItem
          title="Technical support"
          description="We guarantee support and product maintenance after release and
              keep improving the system in cooperation with your team"
        />
        <AdvantagesListItem
          title="Data security"
          description="Your data is stored on secure servers based in Germany (or any
              other country on your request)"
        />
        <AdvantagesListItem
          title="We speak your language"
          description="Our managers are German- and English-speaking, so the business
              communication is clear and easy"
        />
        <AdvantagesListItem
          title="Representative in Germany"
          description="Our business analyst is based in Frankfurt am Main. Discussing all
              the business issues in person is much more efficient"
        />
        <AdvantagesListItem
          title="5 years experience in logistics"
          description="We’ve successfully implemented custom
              logistics/transportation/stock and order management systems"
        />
      </div>
      <div
        class="box box__left flex-column d-flex align-items-center align-items-lg-start"
      >
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
              src="../../assets/img/author-1.png"
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
              src="../../assets/img/author-2.png"
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
import AdvantagesListItem from './advantages-list.vue'
export default { name: 'Advantages', components: { AdvantagesListItem } }
</script>

<style lang="scss" scoped>
.wrap {
  margin: 168px 0 0px 0px;
  width: 77%;

  @include respond-to('md') {
    margin: 168px 0 0px 0px;
  }
  @include respond-to('xs') {
    width: 100%;
    margin: 168px 0 0px 0px;
  }
}

.box {
  width: 45%;
  max-width: 505px;
  margin: 0 54px 0px 0;
  padding: 0 0 40px 0;

  @include respond-to('md') {
    width: 100%;
    max-width: 700px;
    margin: 0 0 96px;
  }

  &__left {
    width: 55%;
    max-width: 633px;
    margin: 0 0px 0 54px;
    padding: 20px 40px;
    box-shadow: 0 10px 30px 0 rgba(0, 0, 0, 0.1);
    background: linear-gradient(140deg, #ffffff, #efefef);

    @include respond-to('md') {
      width: 100%;
      margin: 0 0 0px;
      padding: 20px 0 90px;
    }
  }

  &--title {
    font-size: 35px;
    letter-spacing: -0.88px;
    line-height: 35px;
    font-family: $font-accent;
    text-transform: uppercase;
    margin: 0 0 50px 0;

    @include respond-to('md') {
      font-size: 25px;
      line-height: 25px;
      letter-spacing: -0.63px;
      padding: 0 16px 0;
    }
  }
  &-wrap {
    width: 75%;
    margin: 70px 0;
    &:last-child {
      margin: 0px 0 70px;
    }
    @include respond-to('l') {
      width: 100%;
    }
    @include respond-to('md') {
      width: 75%;
    }
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
}
</style>
