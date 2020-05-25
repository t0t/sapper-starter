<script>
  import Nav from "../components/Nav.svelte";
  import SiteBrand from "../components/SiteBrand.svelte";
  import SiteFooter from "../components/SiteFooter.svelte";
  let active = "active";
  let y = 0;
  export let segment;
</script>

<!-- <style lang="scss" global>
  @import "./styles/main.scss";
  .active {
    position: fixed;
    top: 0;
    z-index: 1;
    background-color: $alpha_white;
  }
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 70px;
    background-color: $light_grey;
  }
</style> -->

<svelte:window bind:scrollY={y} />
<header class:active={y > 100}>
  <SiteBrand sitetitle="TODH" />
  <!-- <SiteNav {segment} /> -->
  <Nav {segment} />
</header>

<main>
  <slot />
</main>

<SiteFooter />
