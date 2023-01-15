<script>
  import { onMount } from 'svelte';
  let stories;

  onMount(async () => {
    const response = await fetch('https://api.hackerwebapp.com/news');
    const data = await response.json();
    stories = data;
  });
</script>

<h1 class="text-3xl font-bold underline">
  Top
</h1>

{#if stories === undefined}
  Loading stories...
{:else}
  {#each stories as story}
    {story.title}<br />
  {/each}
{/if}