<script context="module">
  let current;
</script>

<script>
  export let src;
  export let title;
  export let composer;
  export let performer;

  let audio;
  let paused = true;

  function stopOthers() {
    if (current && current !== audio) current.pause();
    current = audio;
  }
</script>

<style lang="scss">
  // @import "../styles/main.scss";
  //   small {
  //     padding-bottom: 0;
  //     color: $alpha_grey;
  //   }
  // .playing {
  //   color: $secondary;
  //   display: flex;
  // }
  // div {
  //   display: flex;
  //   justify-content: center;
  // }
</style>

<div class:playing={!paused}>
  <small>{title} <br>
    <strong>{composer}</strong>
    / performed by {performer}
  </small>

  <audio bind:this={audio} bind:paused on:play={stopOthers} controls {src} />
</div>