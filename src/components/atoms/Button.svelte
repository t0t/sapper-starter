<script>
  export let text;
  export let href;
</script>

<style lang="scss">
  @import "./styles/main.scss";
  button a {
    background-color: $secondary;
    color: $primary;
    padding-left: $h1;
    padding-right: $h1;
    @include padding-top(0);
    @include padding-bottom(0);
    @include media(s1) {
      @include type-setting(0);
    }

    &:focus {
      outline: none;
    }
    &:hover {
      color: $secondary;
      background-color: $primary;
      cursor: pointer;
    }
    
  }
</style>

<button>
  <a href="{href}">
  {text}
  </a>
</button>
