<script>
  import data from "./products.json";
  export let products = data.products;
</script>

<style lang="scss">
  @import "../../styles/main.scss";
  aside {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  img {
    max-width: 100%;
    height: auto;
    border-radius: 50%;
  }
</style>

<aside>
  {#each products as product}
    <a rel="prefetch" href="products/{product.slug}">
      <img src={product.thumb} alt={product.title} />
    </a>
  {/each}
</aside>
