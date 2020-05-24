<script context="module">
  export async function preload({ params, query }) {
    // the `slug` parameter is available because
    // this file is called [slug].svelte
    const res = await this.fetch(`blog/${params.slug}.json`);
    const data = await res.json();

    if (res.status === 200) {
      return { post: data };
    } else {
      this.error(res.status, data.message);
    }
  }
</script>

<script>
  import SideNav from "./_SideNav.svelte";
  import PageTitle from "../../components/PageTitle.svelte";

  export let post;
</script>

<style lang="scss">
  @import "../../styles/main.scss";
</style>

<svelte:head>
  <title>{post.title}</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">{post.title}</h1>
  <h2 slot="subtitle">---</h2>
</PageTitle>

<div class="grid">
  <div class="col-desk-9">

    <div class="grid">
      <div class="col-desk-3">
        <img src={post.imagen} alt={post.title} />
      </div>
      <div class="col-desk-9">
        <div class="content">
          {@html post.content}
        </div>
      </div>

    </div>
  </div>
  <div class="col-desk-3">
    <SideNav />
  </div>
</div>
