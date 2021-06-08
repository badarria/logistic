<template>
  <div>
    <Header />
    <div class="overflow-wrap">
      <main>
        <About />
        <Issues />
        <Benefits />
        <Advantages />
        <Achievments />
      </main>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from './components/header/header'
import About from './components/about'
import Issues from './components/issues'
import Benefits from './components/benefits/benefits'
import Advantages from './components/advantages/advantages'
import Achievments from './components/achievments/achievments'
import Footer from './components/footer'

export default {
  name: 'App',
  components: {
    Header,
    About,
    Issues,
    Benefits,
    Advantages,
    Achievments,
    Footer
  }
}
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  &.open {
    height: 100vh;
  }
}
</style>
