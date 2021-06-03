<template>
  <div class="">
    <div class="backdrop"></div>

    <div class="modal">
      <div class="d-flex flex-column">
        <div class="modal--close align-self-end" @click="close">
          <span></span><span></span>
        </div>
        <div class="form">
          <h3 class="form--title">let's discuss your business case!</h3>
          <p class="form--description">
            Everything is possible! We will analyze your existing situation,
            discover the bottlenecks and offer a solution that exactly matches
            your business case!
          </p>
          <form class="form--wrap d-flex flex-column">
            <div class=" d-flex justify-content-between flex-wrap">
              <div class="form-item d-flex flex-column">
                <label for="name" class="form-item--label">Firs Name</label
                ><input
                  name="name"
                  type="text"
                  class="form-item--input"
                  placeholder="Klaus"
                />
              </div>
              <div class="form-item d-flex flex-column">
                <label for="lastName" class="form-item--label">Last Name</label
                ><input
                  name="lastName"
                  type="text"
                  class="form-item--input"
                  placeholder="Voormann"
                />
              </div>
              <div class="form-item form-item__email d-flex flex-column">
                <label for="email" class="form-item--label">E-Mail</label
                ><input
                  type="email"
                  name="email"
                  class="form-item--input"
                  placeholder="Klaus.voormann@email.de"
                />
              </div>
              <div class="form-item form-item__textarea d-flex flex-column">
                <label for="" class="form-item--label"
                  >Some brief description or comments</label
                ><textarea
                  class="form-item--input "
                  placeholder="My business case is completely different, so I want to discuss it with you."
                />
              </div>
              <p class="form--text">
                By pressing the “request a consultation” button you agree with
                <a>data protection</a> policy
              </p>
            </div>
            <button
              type="button"
              v-bind:class="{ 'form--btn__submitted': isSubmitted }"
              class="form--btn btn align-self-end"
              @click="submit"
            >
              {{
                isSubmitted
                  ? 'Your request was successfully sent'
                  : 'Request a Consultation'
              }}
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  data() {
    return { isSubmitted: false }
  },
  methods: {
    close() {
      this.$emit('close')
    },
    submit() {
      this.isSubmitted = true
      setTimeout(() => this.$emit('close'), 3000)
    }
  }
}
</script>

<style lang="scss" scoped>
.backdrop {
  backdrop-filter: blur(10px);
  width: 100%;
  height: 100vh;
  z-index: 19;
  overflow-y: hidden;
  background: rgb(48 48 48 / 70%);
  position: fixed;
  left: 0;
  right: 0;
  left: 0;
  bottom: 0;
}

.modal {
  z-index: 20;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 633px;
  box-shadow: 0 10px 30px 0 rgba(30, 30, 30, 0.25);
  background-image: linear-gradient(140deg, #ffffff, #efefef 100%);
  &--close {
    width: 44px;
    height: 44px;
    background: #d6d6d6;
    position: relative;
    border-radius: 0 0px 0px 22px;
    transition: 0.4s all;
    & span {
      position: absolute;
      top: 12px;
      left: 20px;
      display: block;
      width: 4px;
      height: 20px;
      border-radius: 15px;
      transform: rotate(45deg);
      background: $color-black;
    }
    span:nth-child(1) {
      transform: rotate(-45deg);
    }
    &:hover {
      cursor: pointer;
      background: $color-accent;
      transition: 0.4s all;
    }
  }
}

.form {
  position: relative;
  padding: 0px 52px 33px;
  &--title {
    width: 345px;
    font-family: $font-accent;
    font-size: 25px;
    line-height: 30px;
    letter-spacing: -0.63px;
    text-transform: uppercase;
  }
  &--description {
    margin: 20px 0 0;
    letter-spacing: -0.38px;
    font-size: 15px;
    opacity: 75%;
  }
  &--wrap {
    padding: 50px 0px 0;
  }
  &--text {
    width: 345px;
    opacity: 75%;
    letter-spacing: -0.38px;
    font-size: 15px;
    margin: 25px 0 50px 12px;
    & a {
      font-weight: 600;
      text-decoration: underline;
    }
  }
  &--btn {
    padding: 10px 24px;

    &__submitted {
      transition: 0.4s all;
      box-shadow: 0 0 0 2px green;
      background: transparent;
      color: $color-black;

      &:hover {
        cursor: pointer;
        transition: 0.4s all;
        box-shadow: 0 0 0 2px green;
        background: transparent;
        color: $color-black;
      }
    }
  }
  &-item {
    padding: 12px;
    width: 50%;
    &--label {
      margin: 0 0 0 24px;
      font-size: 13px;
      letter-spacing: -0.33px;
    }
    &--input {
      outline: none;
      border-radius: 25px;
      padding: 10px 24px;
      border: 1px solid rgba(30, 30, 30, 0.25);
      &::placeholder {
        letter-spacing: -0.43px;
        font-size: 17px;
        opacity: 25%;
        color: $color-black;
      }
    }
    &__email {
      width: 100%;
    }
    &__textarea {
      width: 100%;
      & textarea {
        resize: none;
        min-height: 132px;
        &::-webkit-scrollbar {
          border-radius: 10px;
        }
      }
    }
  }
}
</style>
