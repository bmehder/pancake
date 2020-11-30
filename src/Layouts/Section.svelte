<script>
  import Blockquote from "../UI/Blockquote.svelte";
  export let background = "";
  export let color = "";
  export let full = false;
</script>

<section class:full style="background:{background};color:{color};">
  <div>
    <slot />
  </div>
</section>

<style>
  section {
    padding: 3rem 4rem;
    background: white;
  }
  div {
    max-width: 960px;
    margin: 0 auto;
    width: 100%;
  }
  .full {
    min-height: 100vh;
  }
  @media screen and (max-width: 480px) {
    .full {
      min-height: initial;
    }
  }
</style>
