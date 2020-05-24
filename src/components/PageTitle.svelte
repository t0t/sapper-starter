<script>
  let y = 0;
</script>

<style lang="scss">
  @import "../styles/main.scss";
  .PageTitleContainer {
    display: flex;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    background-color: $light_grey;
    @include padding-top(3);
    @include padding-bottom(4);
  }
  .PageTitle {
    @include media(s1) {
    }
  }
</style>

<svelte:window bind:scrollY={y} />

<header
  class="PageTitleContainer"
  style=" opacity: {1 - Math.max(0, y / 40)}; ">
  <hgroup class="text-center">
    <slot name="pagetitle" />
    <slot name="subtitle" />
    <slot name="extratitle" />
  </hgroup>
</header>
