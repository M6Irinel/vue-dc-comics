<template>
  <header>
    <div class="container">
      <b-navbar class="flex align-items-lg-stretch p-0" toggleable="lg" type="" variant="">
        <nav class="navbar navbar-light">
          <a class="navbar-brand" href="#">
            <img src="../assets/img/dc-logo.png" width="70" height="70" alt="">
          </a>
        </nav>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse class="flex align-items-stretch h-auto" id="nav-collapse" is-nav>
          <b-navbar-nav class="ms-auto fw-bold">
            <b-nav-item :class="classActiveMenu(0)" @click="goBtnActive(0)" href="#">CHARACTERS</b-nav-item>
            <b-nav-item :class="classActiveMenu(1)" @click="goBtnActive(1)" href="#">COMICS</b-nav-item>
            <b-nav-item :class="classActiveMenu(2)" @click="goBtnActive(2)" href="#">MOVIS</b-nav-item>
            <b-nav-item :class="classActiveMenu(3)" @click="goBtnActive(3)" href="#">TV</b-nav-item>
            <b-nav-item :class="classActiveMenu(4)" @click="goBtnActive(4)" href="#">GAMES</b-nav-item>
            <b-nav-item :class="classActiveMenu(5)" @click="goBtnActive(5)" href="#">COLLECTIBLES</b-nav-item>
            <b-nav-item :class="classActiveMenu(6)" @click="goBtnActive(6)" href="#">VIDEO</b-nav-item>
            <b-nav-item :class="classActiveMenu(7)" @click="goBtnActive(7)" href="#">FANS</b-nav-item>
            <b-nav-item :class="classActiveMenu(8)" @click="goBtnActive(8)" href="#">NEWS</b-nav-item>
            <b-nav-item :class="classActiveMenu(9)" @click="goBtnActive(9)" href="#">SHOP</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </header>
</template>

<script>
export default {
  name: 'MainHeader',
  data () {
    return {
      activeNavMenuBtn: 1
    }
  },
  methods: {
    goBtnActive ( i ) {
      this.activeNavMenuBtn = i;
    },
    classActiveMenu ( i ) {
      return this.activeNavMenuBtn === i ? 'active' : '';
    }
  }
}
</script>

<style scoped lang="scss">
.navbar-nav {
  display: flex;
  gap: 20px;
}

.nav-item {
  display: flex;
  align-items: center;
  letter-spacing: -1px;
  
  a {
    color: #000;
    padding: 0 !important;
    
      &:hover {
        color: gray;
      }
  }

  &.active {
    position: relative;

    a {
      color: #0282f9;
    }

    &::before {
      content: '';
      display: block;
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 6px;
      background-color: #0282f9;
    }
  }
}
</style>