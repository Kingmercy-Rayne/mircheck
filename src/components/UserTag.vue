<template>
  <div class="user-tag">
    <div class="user__img">
      <img src="@/assets/img/nonsap-visuals-kMJp7620W6U-unsplash.jpg" alt="" />
    </div>
    <div class="user__details">
      <p class="user__name">Alexander Podolski</p>
      <p class="user__status">
        PRO
        <span>online</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserTag',
};
</script>

<style lang="stylus" scoped>
.user-tag {
  height: 100%;
  display: flex;
  align-items: center;
  color: var(--text-color--primary);

  .user__img {
    display: flex;
    justify-content: center;
    align-items: center;

    // padding: 1em;
    // width: 2rem;
    // height: 2rem;
    // overflow: none;
    img {
      width: 3em;
      height: 3em;
      border-radius: 50%;
      border: solid 2px brown;
      object-fit: cover;
      object-position: top top;
    }
  }

  .user__details {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0 0.5em;
    font-size: 0.8rem;
    letter-spacing: 1.2px;

    .user__name {
      // font-size: 1.2rem;
    }

    .user__status {
      font-size: 0.7rem;

      span {
        color: var(--text-color--alt);
      }
    }
  }
}
</style>
