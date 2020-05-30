<template>
  <li class="user-expense__item">
    <i class="service__logo fab fas fa" :class="icon" :style="{ color: color, background: bg }"></i>
    <h5 class="service__name">{{ service }}</h5>
    <h6 class="service__bill">{{ bill }}</h6>
  </li>
</template>

<script>
export default {
  name: 'UserExpenseItem',
  props: ['service', 'bill', 'icon', 'color', 'bg'],
};
</script>
<style lang="stylus" scoped>
.user-expense__item {
//   border: solid thin green;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0.2em 0.8em;
  text-align: center;

  .service__logo {
    border-radius: 50%;
    padding: 0.4em 0.5em;
    margin-bottom: 0.6em;
    font-size: 1.2rem;
    color: var(--text-color--primary);
    background: black;
  }

  .service__name {
    padding: 0.2em 0;
    color: var(--text-color--primary);
    font-weight: 600;
    text-transform: capitalize;
    letter-spacing: 0.05rem;
  }

  .service__bill {
    color: var(--text-color--primary);
    font-weight: 600;
    letter-spacing: 0.05rem;
    opacity: 0.8;
  }
}
</style>
