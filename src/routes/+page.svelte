<script lang="ts">
	import Header from '$lib/components/Header.svelte';
</script>

<div class="min-h-screen flex flex-col">
	<div class="p-2">
		<Header />
	</div>

	<main class="flex-grow container mx-auto px-4 py-8">
		<slot />
	</main>
</div>
