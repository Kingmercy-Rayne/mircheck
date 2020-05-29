<template>
  <div class="page home">
    <section class="section1">
      <user-wallets />
    </section>
    <section class="section2"></section>
    <section class="section3"></section>
  </div>
</template>

<script>
// @ is an alias to /src
import UserWallets from '@/components/UserWallets.vue';

export default {
  name: 'Home',
  components: {
    UserWallets,
  },
};
</script>
<style lang="stylus" scoped>
.home {
  border: solid thin green;
  width: 100%;
  padding-top: 10vh;
  padding-left: var(--padding-L--global);
  padding-right: var(--padding-R--global);
  min-height: 100vh;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(8, 1fr);
  grid-column-gap: 0.5em;
  grid-row-gap: 0.5em;

  .section1 {
    grid-area: 1 / 1 / 9 / 3;
    border: solid thin green;
  }

  .section2 {
    grid-area: 1 / 3 / 5 / 4;
    display: flex;
    flex-direction: column;
    border: solid thin green;
  }

  .section3 {
    grid-area: 5 / 3 / 9 / 4;
    border: solid thin green;
  }
}
</style>
