<script>
  import '../app.scss';
  
  import Header from '$lib/Header.svelte';
</script>

<div class="flex min-h-screen flex-col">
  <Header />
	<div class="flex flex-1 flex-row bg-gray-50">
		<div class="col-start-2">
			<!-- Here you can place your Navigation -->
		</div>
		<div>
      <main class="flex p-4">
        <slot />
      </main>
		</div>
	</div>
  <footer class="bg-blue-200 p-4">Footer</footer>
</div>
