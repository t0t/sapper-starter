<script>
  import { getContext } from "svelte";
  import { TABS } from "./Tabs.svelte";

  const tab = {};
  const { registerTab, selectTab, selectedTab } = getContext(TABS);

  registerTab(tab);
</script>

<style lang="scss">
  @import "../../styles/main.scss";
  button {
	  transition: color .3s linear;
    &:hover {
      color: $grey;
	}	
  }
</style>

<button class:selected={$selectedTab === tab} on:click={() => selectTab(tab)}>
  <slot />
</button>
