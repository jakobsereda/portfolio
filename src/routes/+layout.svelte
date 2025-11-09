<script lang="ts">
	import "../app.css";
	import "../global.css";
	import Header from "$lib/components/Header.svelte";
	import Footer from "$lib/components/Footer.svelte";

	let { children } = $props();
</script>

<div class="font-display mx-auto px-8 min-h-screen max-w-3xl flex flex-col">
	<div class="pt-16 pb-4">
		<Header />
	</div>

	<main class="flex-1">
		{@render children()}
	</main>

	<footer class="pt-4 pb-4">
		<Footer />
	</footer>
</div>
