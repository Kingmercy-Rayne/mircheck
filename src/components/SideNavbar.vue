<template>
  <div class="side-navbar">
    <div class="site__logo">
      <the-logo />
      <ul class="nav__list">
        <navigation-item
          v-for="(item, index) in NavigationItems"
          :key="index"
          :icon="item.icon"
          :urlFor="item.urlFor"
          :isActive="item.isActive"
        />
      </ul>
    </div>
  </div>
</template>

<script>
import TheLogo from '@/components/TheLogo.vue';
import NavigationItem from '@/components/NavigationItem.vue';

export default {
  name: 'SideNavbar',
  components: {
    TheLogo,
    NavigationItem,
  },
  data() {
    return {
      NavigationItems: [
        { icon: 'fa-bar-chart', urlFor: 'dashboard', isActive: true },
        { icon: 'fa-pencil-square-o', urlFor: 'buy/sell' },
        { icon: 'fa-newspaper-o', urlFor: 'news' },
        { icon: 'fa-credit-card', urlFor: 'send money' },
        { icon: 'fa-plus-circle', urlFor: 'deposit' },
        { icon: 'fa-book', urlFor: 'transactions' },
        { icon: 'fa-user', urlFor: 'account' },
        { icon: 'fa-cogs', urlFor: 'settings' },
      ],
    };
  },
};
</script>

<style lang="stylus" scoped>
.side-navbar {
  position: fixed;
  z-index: 20;
  left: 0;
  top: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  background: var(--bg-color--alt);
  box-shadow: 4px 0px 3px 0px rgba(0, 0, 0, 0.1);

  .nav__list {
    width: 100%;
    min-height: 50vh;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: 2em 0.2em;
    // border:solid thin brown;
  }
}
</style>
