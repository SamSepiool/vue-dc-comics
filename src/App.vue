<template>
  <div id="app">
    <Header/>
    <main>
      <Content/>
      <Services/>
    </main>
    <Footer/>
    
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Content from "./components/Content.vue"
import Services from "./components/Services.vue"
import Footer from "./components/Footer.vue"





export default {
  name: 'App',
  components: {
      Header,
      Content,
      Services,
      Footer
  }
}
</script>


<style lang="scss">
@import "./assets/style/common"

</style>
