<script lang="ts">
	import "../app.css";
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<div class="font-display mr-auto ml-auto pr-8 pl-8 min-h-screen max-w-3xl flex flex-col">
	<div class="pt-16"> 
		<Header />
	</div>

	<div>
		{@render children()}
	</div>

	<Footer />
</div>
