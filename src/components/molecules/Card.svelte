<script>
  export let cardtitle;
</script>

<!-- <style lang="scss">
  @import "../../styles/main.scss";
  .Card {
    margin: $h0;
  }
</style> -->

<div class="Card">
  <slot name="title">
    <h5 class="CardTitle">{cardtitle}</h5>
  </slot>
  <slot />
</div>
