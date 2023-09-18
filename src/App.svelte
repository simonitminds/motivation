<script lang="ts">
  import { motivationalQuotesNorwegian } from "./lib/the_quotes";

  // random number between 1 and 20
  const num = Math.floor(Math.random() * 20) + 1;
</script>

<main>
  <div>
    {motivationalQuotesNorwegian[num]}
  </div>
</main>

<style>
</style>
