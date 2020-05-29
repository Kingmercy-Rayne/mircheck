<template>
  <h2 class="submenu__header"></h2>
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
  border: solid thin cyan;
  min-height: 10vh;
  display: flex;
}
</style>
