<template>
  <nav class="navbar">
    <user-tag />
    <button class="btn--mid btn--alt-color">
      <i class="fas fa fa-retweet"></i>
      Quick Transaction
    </button>
    <v-search />
  </nav>
</template>

<script>
import VSearch from '@/components/VSearch.vue';
import UserTag from '@/components/UserTag.vue';

export default {
  name: 'TheNavbar',
  components: {
    UserTag,
    VSearch,
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
  padding: 0.4em 0.1em;
  padding-left: var(--padding-L--global);
  padding-right: var(--padding-R--global);
  background: var(--bg-color--primary);
//   border: solid thin yellow;

  @media screen and (max-width: 480px) {
    padding: 0.4em 5%;
  }
}
</style>
