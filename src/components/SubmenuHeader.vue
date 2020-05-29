<template>
  <h4 class="submenu__header">
    <span>wallets</span>
    <i class="fas fa fa-ellipsis-h"></i>
  </h4>
</template>

<script>
export default {
  name: 'SubmenuHeader',
  props: ['nameTag'],
};
</script>
<style lang="stylus" scoped>
.submenu__header {
  width: 100%;
//   border: solid thin cyan;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em 0;
  text-transform: capitalize;
  color: var(--text-color--primary);
  font-family: var(--font-family--alt);
  font-weight: 400;

  i {
    font-weight: 400;
    font-size: 1rem;
  }
}
</style>
