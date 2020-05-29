<template>
  <div class="user-wallet__item">
    <i class="wallet__item__img fab fa" :class="logo" :style="{ color: color }"></i>
    <div class="wallet__item__details">
      <h4 class="wallet__item__header">
        <span>{{ abbr }}</span> <span>({{ tagName }})</span>
      </h4>
      <div class="item__category">
        <h6 class="item__category__ref">Balance</h6>
        <h4 class="item__category__value">{{ balance }}</h4>
      </div>
      <div class="item__category">
        <h6 class="item__category__ref">USD</h6>
        <h6 class="item__category__value">{{ usd }}</h6>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserWalletItem',
  props: ['logo', 'color', 'abbr', 'tagName', 'balance', 'usd'],
};
</script>
<style lang="stylus" scoped>
.user-wallet__item {
  // border: solid thin blue;
  min-height: 15vh;
  background: var(--bg-color--alt);
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 1em 1.5em;
  border-radius: 0.4em;
  color: var(--text-color--primary);

  .wallet__item__img {
    border-radius: 50%;
    background: white;
    color: var(--text-color--alt);
    font-size: 1.3rem;
    padding: 0.3em 0.4em;
  }

  .wallet__item__details {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 1em;

    .wallet__item__header {
      margin-bottom: 1em;
    }

    .item__category {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      min-width: 12vw;
      padding: 0.3em 0;
      text-align: left;

      .item__category__ref {
        flex-basis: 50%;
        font-weight: 800;
      }

      .item__category__value {
        flex-basis: 50%;
        flex-grow: 1;
        font-family: var(--font-family--alt);
        font-weight: 600;
      }
    }
  }
}
</style>
