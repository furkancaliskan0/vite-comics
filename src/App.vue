<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter
    

  }
}
</script>

<template>
  <AppHeader/>
  <main>
    <h1>--> Content goes hear &lt;--</h1>
  </main>
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/partials/variables' as*;
@use './styles/general.scss' as*;
@use './styles/partials/mixins' as*;

main {
  height: 100px;
  background-color: #131212;
  text-align: center;
  line-height: 100px;
}


h1,
h3,
h6,
button {
  color: $primary;
}
a{
  color: $third;
}

</style>
