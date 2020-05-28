<template>
  <div id="app">
    <the-navbar />
    <side-navbar />
    <router-view />
  </div>
</template>
<script>
import TheNavbar from '@/components/TheNavbar.vue';
import SideNavbar from '@/components/SideNavbar.vue';

export default {
  components: {
    SideNavbar,
    TheNavbar,
  },
};
</script>

<style lang="stylus">
#app {
  position: relative;
  min-height: 100vh;
  width: 100%;
  font-family: var(--font-family--primary);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: var(--bg-color--primary);
  color: #2c3e50;
}
</style>
