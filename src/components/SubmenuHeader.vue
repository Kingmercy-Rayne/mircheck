<template>
  <h5 class="submenu__header">
    <span>{{ nameTag }}</span>
    <i class="fas fa fa-ellipsis-h"></i>
  </h5>
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
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em 0;
  text-transform: capitalize;
  color: var(--text-color--primary);
  font-family: var(--font-family--alt);
  font-weight: 600;

  i {
    font-weight: 400;
    font-size: 1rem;
  }
}
</style>
