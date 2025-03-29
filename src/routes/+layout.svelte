<script lang="ts">
	import "../app.css";
	import Header from '$lib/components/Header.svelte';

	let { children } = $props();
</script>

<div class="font-display p-8 min-h-screen flex flex-col gap-4">
	<div class="border-2 border-gruvbox-fg4 border-solid"> 
		<Header />
	</div>

	<div class="border-2 border-gruvbox-fg4 border-solid grow flex flex-col">
		{@render children()}
	</div>
</div>
