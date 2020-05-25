<script context="module">
  export async function preload({ params, query }) {
    const res = await this.fetch(`blog/${params.slug}.json`);
    const post = await res.json();

    if (res.status === 200) {
      return { post: post };
    } else {
      this.error(res.status, post.message);
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
