<script context="module">
  export async function preload({ params, query }) {
    const res = await this.fetch(`products/${params.slug}.json`);
    const products = await res.json();

    if (res.status === 200) {
      return { product: products };
    } else {
      this.error(res.status, products.message);
    }
  }
</script>

<script>
  import Content from "../../components/layouts/Content.svelte";
  import PageTitle from "../../components/PageTitle.svelte";
  import SideNav from "./_SideNav.svelte";
  import { fade } from "svelte/transition";
  export let product;
  let i = 0;
  const next = () => {
    let num = product.subthumb;
    i = (i + 1) % num.length;
  };
</script>

<style>
  .subthumbs img {
    padding: 20px;
    width: 150px;
    border-radius: 50%;
  }
</style>

<svelte:head>
  <title>TODH | obras | {product.title}</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">{product.title}</h1>
</PageTitle>

<Content>

  <div class="col-desk-10 col-tab-9 col-mob-4">
    <img src={product.imagen} alt={product.title} />
    <div class="content">
      {@html product.content}

      <div class="grid subthumbs">
        {#each [product.subthumb[i].img] as src, i (src)}
          <img transition:fade {src} alt="Imagen de detalle" />
          <button on:click={next}>Next Detail -></button>
        {/each}
      </div>
    </div>
  </div>
  <div class="col-desk-2 col-tab-1 col-mob-4">
    <SideNav />
  </div>

</Content>
