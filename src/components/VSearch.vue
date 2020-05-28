<template>
  <div class="v-search">
    <form action="" @submit.prevent>
      <input
        type="search"
        name="search"
        placeholder="Search"
        aria-label="Search for a transaction"
      />
      <button type="submit" class="btn--border-alt"><i class="fas fa fa-search"></i></button>
    </form>
  </div>
</template>

<script>
// import { mapState } from 'vuex';

export default {
  name: 'VSearch',
};
</script>

<style lang="stylus" scoped>
.v-search {
  // border: solid thin brown;
  // padding: 0.5em;
  width: 20%;
  font-family: var(--font-family--primary);

  @media screen and (max-width: 800px) {
    width: 50%;
  }

  @media screen and (max-width: 480px) {
    flex-grow: 1;
  }

  // height:100%;
  form {
    // set padding for button and input
    --form-padding: 0.5em;
    position: relative;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    border-radius: 0.8em;
    border: solid thin var(--border-color--alt);
    background: var(--search-area-bg);

    input {
      width: 100%;
      padding: var(--form-padding);
      background: none;
      color: #000;
      border: none;
      font-size: 0.8rem;

      @media screen and (max-width: 800px) {
        font-size: 0.6rem;
      }
    }

    button {
      // border: solid thin green;
      top: 0;
      right: 0;
      bottom: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: var(--form-padding);
      background: transparent;

      i {
        color: var(--text-color--tri);
        font-size: 0.8rem;

        @media screen and (max-width: 800px) {
          font-size: 0.6rem;
        }
      }
    }
  }
}
</style>
