<template>
  <div class="user-wallets">
    <submenu-header nameTag="wallets" />
    <ul class="wallet__item__list">
      <user-wallet-item
        v-for="(item, index) in walletItems"
        :key="index"
        :logo="item.logo"
        :color="item.color"
        :abbr="item.abbr"
        :tagName="item.tagName"
        :balance="item.balance"
        :usd="item.usd"
      />
      <i class="wallet__item__paginator fas fa fa-angle-right"></i>
    </ul>
    <path-informer />
  </div>
</template>

<script>
import SubmenuHeader from '@/components/SubmenuHeader.vue';
import UserWalletItem from '@/components/UserWalletItem.vue';
import PathInformer from '@/components/PathInformer.vue';

export default {
  name: 'UserWallets',
  components: {
    SubmenuHeader,
    UserWalletItem,
    PathInformer,
  },
  data() {
    return {
      walletItems: [
        {
          logo: 'fa-btc',
          color: 'orange',
          abbr: 'BTC',
          tagName: 'Bitcoin',
          balance: '1,177.10',
          usd: '7,628,220.31',
        },
        {
          logo: 'fa-first-order',
          color: 'green',
          abbr: 'ETH',
          tagName: 'Ether',
          balance: '480.21',
          usd: '30,192.31',
        },
      ],
    };
  },
};
</script>

<style lang="stylus" scoped>
.user-wallets {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  .wallet__item__list {
    display: flex;
    width: 100%;
    justify-content: space-between;

    .wallet__item__paginator {
      align-self: center;
      color: var(--text-color--primary);
      padding: 1em;
      text-align: left;
      margin-right: 1em;
    }
  }
}
</style>
