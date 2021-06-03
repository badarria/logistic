<template>
  <div>
    <Header />
    <div class="overflow-wrap">
      <main>
        <Scroll />
        <About />
        <Issues />
        <Benefits />
        <!-- <ConsultationForm /> -->
        <Advantages />
        <Achievments />
      </main>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import About from './components/About.vue'
import Issues from './components/Issues.vue'
import Benefits from './components/Benefits.vue'
// import ConsultationForm from './components/ConsultationForm.vue'
import Advantages from './components/Advantages.vue'
import Achievments from './components/Achievments.vue'
import Footer from './components/Footer.vue'
import Scroll from './components/Scroll.vue'

export default {
  name: 'App',
  components: {
    Header,
    About,
    Issues,
    Benefits,
    // ConsultationForm,
    Advantages,
    Achievments,
    Footer,
    Scroll
  }
}
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
