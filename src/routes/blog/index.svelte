<script context="module">
  // export function preload({params, query}) {
  //   return this.fetch(`blog.json`)
  //   let posts = res.json()

  // }
  // export async function preload(page) {
	// 	const query = page.query
	// 	const res = await this.fetch(`products.json`)

	// 	let products = await res.json()

	// 	return {products}
	// }
</script>



<script>
  import data from "./blog.json";
  export let posts = data.posts;
  import PageTitle from "../../components/PageTitle.svelte";
</script>

<style lang="scss">
  @import "../../styles/main.scss";
  section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    // grid-gap: $h2;
  }
</style>

<svelte:head>
  <title>Blog</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">Recent posts</h1>
  <h2 slot="subtitle">---</h2>
</PageTitle>

<div class="grid">
  <section>
    {#each posts as post}
      <article>
        <a rel="prefetch" href="blog/{post.slug}">
          <h6>{post.title}</h6>
          <img src={post.thumb} alt="" />
          <p>{post.description}</p>
        </a>
      </article>
    {/each}
  </section>
</div>
