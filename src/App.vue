<template>
  <div id="app">
    <Header/>
    <main>
      <Content/>
      <Services/>
    </main>
    
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Content from "./components/Content.vue"
import Services from "./components/Services.vue"



export default {
  name: 'App',
  components: {
      Header,
      Content,
      Services
  }
}
</script>


<style lang="scss">
@import "./assets/style/common"

</style>
