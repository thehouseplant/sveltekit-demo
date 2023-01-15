<script>
  import '../app.scss';
  
  import Header from '$lib/Header.svelte';
</script>

<main>
  <Header />
	<article class="grid h-screen place-content-center">
		<div class="col-start-2">
			<!-- Here you can place your Navigation -->
		</div>
		<div>
			<slot />
		</div>
	</article>
</main>
