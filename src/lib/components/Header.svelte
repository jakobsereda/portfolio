<script lang="ts">
	import { page } from '$app/state';

	const items = [
		{ route: '/',         label: 'Home'     },
		{ route: '/projects', label: 'Projects' },
		{ route: '/music',    label: 'Music'    },
	];
</script>

<div class="p-2 pr-4 pl-4 bg-gruvbox-bg2 flex flex-row justify-around gap-2">
	<span class="w-1/2 font-semibold text-gruvbox-fg0">
		Jakob's <span class="text-gruvbox-green1">Portfolio</span>
	</span>
	<span>
	</span>
	<div class="w-1/2 flex gap-8 justify-end">
	{#each items as item (item.route)}
		<a href={item.route} class="font-semibold underline {page.url.pathname === item.route ? 'text-gruvbox-green1' : 'text-gruvbox-fg0'}">
			{item.label}
		</a>
	{/each}
	</div>
</div>
