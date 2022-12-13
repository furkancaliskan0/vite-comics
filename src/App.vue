<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import Jumbotron from './components/Jumbotron.vue'

export default {
  components:{
    AppHeader,
    Jumbotron,
    AppMain,
    AppFooter
    
    

  }
}
</script>

<template>
  <AppHeader />
  <jumbotron />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/partials/variables' as*;
@use './styles/general.scss' as*;
@use './styles/partials/mixins' as*;



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
