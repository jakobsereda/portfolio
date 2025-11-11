<script lang="ts">
	import AboutMe from '$lib/components/AboutMe.svelte';
	import HireMe from '$lib/components/HireMe.svelte';
	import ContactMe from '$lib/components/ContactMe.svelte';
</script>

<div class="flex flex-col gap-4 text-justify text-gruvbox-bg0 dark:text-gruvbox-fg0 text-sm">
	<div class="flex flex-row gap-4">
		<img src="./jakegreen.png" alt="jakegreen" class="h-100 w-auto hidden dark:block" />
		<img src="./jakeblue.png" alt="jakblue" class="h-100 w-auto block dark:hidden" />
		<AboutMe />
	</div>
	<HireMe />
	<ContactMe />
</div>
