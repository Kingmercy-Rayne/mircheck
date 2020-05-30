<template>
  <div class="user-expenses">
    <submenu-header nameTag="expenses" />
    <ul class="expenses__list">
      <user-expense-item
        v-for="(item, index) in expenseList"
        :key="index"
        :service="item.service"
        :bill="item.amount"
        :icon="item.icon"
        :color="item.color"
        :bg="item.bg"
      />
    </ul>
    <path-informer />
  </div>
</template>

<script>
import SubmenuHeader from '@/components/SubmenuHeader.vue';
import UserExpenseItem from '@/components/UserExpenseItem.vue';
import PathInformer from '@/components/PathInformer.vue';

export default {
  name: 'UserExpenses',
  components: {
    SubmenuHeader,
    UserExpenseItem,
    PathInformer,
  },
  data() {
    return {
      expenseList: [
        {
          service: 'paypal',
          amount: '$200',
          icon: 'fa-paypal',
          color: '#253B80',
          bg: '#fff',
        },
        {
          service: 'amazon',
          amount: '$1832',
          icon: 'fa-amazon',
          color: '#fff',
          bg: '#FF9900',
        },
        {
          service: 'apple',
          amount: '$3200',
          icon: 'fa-apple',
          color: '#000',
          bg: '#fff',
        },
        {
          service: 'google',
          amount: '$40',
          icon: 'fa-google',
          color: '#3369EB',
          bg: '#fff',
        },
        {
          service: 'spotify',
          amount: '$55',
          icon: 'fa-spotify',
          color: '#1ED761',
          bg: '#000',
        },
        {
          service: 'steam',
          amount: '$9280',
          icon: 'fa-steam',
          color: '#fff',
          bg: '#1b2838',
        },
        {
          service: 'adobe',
          amount: '$600',
          icon: 'fa-buysellads',
          color: '#fff',
          bg: '#FF0000',
        },
      ],
    };
  },
};
</script>
<style lang="stylus" scoped>
.user-expenses {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  .expenses__list {
    width: 100%;
    // border: solid thin cyan;
    min-height: 20vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}
</style>
