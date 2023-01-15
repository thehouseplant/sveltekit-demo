<script>
  import { onMount } from 'svelte';
  let stories;

  onMount(async () => {
    const response = await fetch('https://api.hackerwebapp.com/news');
    const data = await response.json();
    stories = data;
  });
</script>

<div>
  <h1>
    Top
  </h1>

  {#if stories === undefined}
    Loading stories...
  {:else}
    {#each stories as story}
      <div class="mx-auto max-w-xlg rounded-lg bg-white shadow mb-6">
        <div class="p-4">
          {story.title} ({ story.domain })<br />
          {story.points} points
          by {story.user} | 
          Posted { story.time_ago } | {story.comments_count} comments
        </div>
      </div>
    {/each}
  {/if}
</div>