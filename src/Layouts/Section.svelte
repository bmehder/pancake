<script>
  import Blockquote from "../UI/Blockquote.svelte";
  export let background = "";
  export let color = "";
  export let full = false;
</script>

<section class:full style="background:{background};color:{color};">
  <slot />
</section>

<style>
  section {
    max-width: 960px;
    margin: 0 auto;
    padding: 2rem 4rem;
    background: white;
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
