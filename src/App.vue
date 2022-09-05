<template>
  <div id="app" class="container">
    <MainHeader/>
    <MainMain/>
    <MainFooter/>
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainMain from './components/MainMain.vue';
import MainFooter from './components/MainFooter.vue';

export default {
  name: 'App',
  components: {
    MainHeader,
    MainMain,
    MainFooter
  }
}
</script>

<style lang="scss">

</style>
