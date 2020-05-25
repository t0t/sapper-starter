<!-- <script context="module">
	export async function preload(page) {
		const query = page.query
		const res = await this.fetch(`products.json`)

		let products = await res.json()

		return {products}
	}
</script> -->

<script>
  import data from "./products.json";
  export let products = data.products;

  import PageTitle from "../../components/PageTitle.svelte";
  import Content from "../../components/layouts/Content.svelte";
  import Blockquote from "../../components/molecules/Blockquote.svelte";
  import Figure from "../../components/molecules/Figure.svelte";
  import CardGroup from "../../components/molecules/CardGroup.svelte";
  import Card from "../../components/molecules/Card.svelte";
</script>

<svelte:head>
  <title>Artwork</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">Obra plástica</h1>
  <h2 slot="subtitle">Emoción cristalizada</h2>
</PageTitle>

<Content>

  <div class="col-desk-6 col-tab-5 col-mob-4">
    <Figure src="img/detalle1.jpg" alt="Alt de imagen" caption="Estudio" />
    <Blockquote
      quote="Lo más importante en la vida es que lo más importante sea lo más
      importante"
      author="STEPHEN COVEY" />
  </div>
  <div class="col-desk-6 col-tab-5 col-mob-4">
    <p>
      Me gusta explorar los juegos de luces y sombras sobre la superficie del
      cuadro, las texturas, los volúmenes, etc. Últimamente me encuentro cómodo
      ideando mis cuadros en el ordenador para luego imprimirlos en 3D y
      terminarlos en la postproducción.
    </p>
  </div>

  <div class="col-desk-12 col-tab-10 col-mob-4">
    <CardGroup>
      {#each products as product}
        <Card cardtitle={product.title}>
          <a href="products/{product.slug}">
            <Figure src={product.thumb} alt={product.title} />
          </a>
        </Card>
      {/each}
    </CardGroup>
  </div>

</Content>
