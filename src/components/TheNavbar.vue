<template>
  <nav class="navbar">
    <the-logo />
    <button class="btn--mid btn--alt-color">Quick Transaction</button>
  </nav>
</template>

<script>
// import TheLogo from '@/components/TheLogo.vue';

export default {
  name: 'TheNavbar',
  components: {
    // TheLogo,
  },
};
</script>

<style lang="stylus" scoped>
.navbar {
  position: fixed;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  min-height: 10vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.4em var(--padding-LR--global);
  background: var(--bg-color--primary);
  border: solid thin yellow;

  @media screen and (max-width: 480px) {
    padding: 0.4em 5%;
  }
}
</style>
