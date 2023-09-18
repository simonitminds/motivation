<script lang="ts">
  import { fly } from "svelte/transition";
  import { motivationalQuotesNorwegian } from "./lib/the_quotes";
  let currentQuote = motivationalQuotesNorwegian[0];
  let index = 0;

  const updateQuote = () => {
    currentQuote = motivationalQuotesNorwegian[index];
    index = (index + 1) % motivationalQuotesNorwegian.length;
  };

  setInterval(updateQuote, 5000); // Update quote every 5 seconds
</script>

<div class="quote-container">
  <div transition:fly={{ y: 0, duration: 1000 }}>
    {currentQuote}
  </div>
</div>

<style>
  .quote-container {
    position: relative;
    overflow: hidden;
  }
</style>
