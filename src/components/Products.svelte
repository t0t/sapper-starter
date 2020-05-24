<script>
  import { onMount } from "svelte";

  let data = [];
  let productos = [];

  onMount(async () => {
    const res = await fetch("db.json");
    data = await res.json();
    productos = data.productos;
    console.log(productos);
  });
</script>

<style>
  .photos {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-gap: 8px;
  }
</style>

<h2 class="col-tab-10">Photo album</h2>

<div class="photos">
  {#each productos as producto}
    <figure>
      <img src={producto.imagen} alt={producto.description} />
      <figcaption>{producto.name}</figcaption>
    </figure>
  {:else}
    <!-- this block renders when photos.length === 0 -->
    <p>loading...</p>
  {/each}
</div>
