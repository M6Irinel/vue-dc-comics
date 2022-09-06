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
            <b-nav-item v-for="(el, i) in HeaderButton" :key="i" :class="classActiveMenu(i)" @click="goBtnActive(i)" :href="el.href"> {{el.content}} </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </header>
</template>

<script>
import HeaderButton from '@/assets/jsons/header- button.json';

export default {
  name: 'MainHeader',
  data () {
    return {
      activeNavMenuBtn: 1,
      HeaderButton
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
      height: 5px;
      background-color: #0282f9;
    }
  }
}
</style>