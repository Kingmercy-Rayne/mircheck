<template>
  <li class="navigation__item" :class="isActive ? 'is-active' : ''">
    <i class="fas fa" :class="icon"></i>
    <span>{{ urlFor }}</span>
  </li>
</template>

<script>
export default {
  name: 'NavigationItem',
  props: ['urlFor', 'icon', 'isActive'],
};
</script>
<style lang="stylus" scoped>
.navigation__item {
  display: flex;
  width: 100%;
  margin: 0.5em 0;
  color: var(--text-color--primary);
  font-size: 0.8rem;

  &:hover {
    color: var(--text-color--tri);
  }

  i {
    padding: 1em 1.5em;
    font-size: 1rem;
    // border: solid thin green;
  }

  span {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding-right: 3em;
    padding-left: 1em;
    text-transform: capitalize;
  }
}

.is-active {
  color: var(--text-color--tri);
}
</style>
