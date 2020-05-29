<template>
  <div class="user-wallets">
    <submenu-header />
  </div>
</template>

<script>
import SubmenuHeader from '@/components/SubmenuHeader.vue';

export default {
  name: 'UserWallets',
  components: {
    SubmenuHeader,
  },
};
</script>

<style lang="stylus" scoped>
.user-wallets {
  border: solid thin brown;
  width: 100%;
  min-height: 30vh;
}
</style>
