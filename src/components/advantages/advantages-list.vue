<template>
  <div class="item d-flex " @click="changeState">
    <div class="item--point"></div>
    <div class="item-content">
      <div
        class="item-content--title d-flex justify-content-between align-items-center"
      >
        <p>{{ title }}</p>
        <img
          src="../../assets/img/pin-left.png"
          alt=""
          class="item-content--arrow"
          v-bind:class="{ active: isOpen }"
        />
      </div>
      <div class="item-content--descr">
        <div class="item-content--hidden" v-bind:class="{ active: isOpen }">
          <div
            class="item-content--hidden__opacity"
            v-bind:class="{ active: isOpen }"
          >
            <p>
              {{ description }}
            </p>
          </div>
        </div>
        <div class="item-content--visible"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AdvantagesListItem',
  props: ['title', 'description'],
  data() {
    return { isOpen: false }
  },
  methods: {
    changeState() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style lang="scss" scoped>
.item {
  margin: 26px 0 0;

  @include respond-to('sm') {
    margin: 0;
  }
  &--point {
    width: 34px;
    height: 34px;
    background: $color-watermelon;
    border-radius: 50%;
    @include respond-to('sm') {
      display: none;
    }
  }

  &-content {
    width: 80%;
    margin: 0 0 0 32px;

    @include respond-to('sm') {
      font-size: 15px;
      letter-spacing: -0.38px;
      width: 100%;
      margin: 0 0 0 0px;
    }
    &--descr {
      overflow: hidden;
      transition: all 0.3s;
    }

    &--visible {
      transition: all 0.3s;
      @include respond-to('sm') {
        width: 100%;
        height: 1px;
        background: #f3f3f3;
      }
    }
    &--hidden {
      @include respond-to('sm') {
        transform: translateY(-100%);
        opacity: 0;
        transition: all 0.3s;

        &.active {
          transform: translateY(0);
          transition: all 0.3s;
          opacity: 1;
        }
      }
      &__opacity {
        @include respond-to('sm') {
          display: none;
          transition: all 0.3s;
          padding: 0 16px 10px;

          &.active {
            transition: all 0.3s;
            display: block;
          }
        }
      }
    }

    &--title {
      font-size: 21px;
      letter-spacing: -0.53px;
      font-family: $font-accent;

      @include respond-to('sm') {
        box-shadow: 0 -1px 0 0 #f3f3f3;
        height: 56px;
        padding: 0 16px 0;
      }
    }

    &--arrow {
      display: none;

      @include respond-to('sm') {
        display: block;
        transition: all 0.3s;

        &.active {
          transition: all 0.3s;
          transform: rotate(180deg);
        }
      }
    }
  }
}
</style>
