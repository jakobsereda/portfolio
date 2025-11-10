<script lang="ts">
	import '../app.css';
	import '../global.css';
	import { browser } from '$app/environment';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();

	if (browser) {
		if (localStorage.theme === 'dark'
			|| (!('theme' in localStorage) 
			&& window.matchMedia('(prefers-color-scheme: dark)').matches)
		) {
			document.documentElement.classList.add('dark');
		} else {
			document.documentElement.classList.remove('dark');
		}
	}
</script>

<div class="font-display bg-gruvbox-fg0 dark:bg-gruvbox-bg0">
	<div class="mx-auto px-8 min-h-screen max-w-3xl flex flex-col">
		<div class="pt-8 pb-4">
			<Header />
		</div>

		<main class="flex-1">
			{@render children()}
		</main>

		<footer class="pt-4 pb-4">
			<Footer />
		</footer>
	</div>
</div>
