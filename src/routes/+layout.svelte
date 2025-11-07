<script lang="ts">
	import "../app.css";
	import Header from '$lib/components/Header.svelte';

	let { children } = $props();
</script>

<div class="font-display mr-auto ml-auto min-h-screen max-w-3xl flex flex-col">
	<div class="p-4"> 
		<Header />
	</div>

	<div class="border-2 border-gruvbox-fg4 border-solid grow flex flex-col">
		{@render children()}
	</div>
</div>
