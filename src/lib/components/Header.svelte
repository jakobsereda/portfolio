<script lang="ts">
	import { page } from '$app/state';

	const items = [
		{ route: '/',         label: 'Home'     },
		{ route: '/projects', label: 'Projects' },
		{ route: '/blog',     label: 'Blog'     },
		{ route: '/music',    label: 'Music'    },
	];
</script>

<div class="flex flex-col">
	<div class="flex flex-row justify-around">
		<span class="w-1/2 font-semibold text-gruvbox-fg0">
			Jakob's Website
		</span>
		<div class="w-1/2 flex gap-8 justify-end">
		{#each items as item (item.route)}
			<a href={item.route} class="font-semibold underline {page.url.pathname === item.route ? 'text-gruvbox-red1' : 'text-gruvbox-fg0'}">
				{item.label}
			</a>
		{/each}
		</div>
	</div>
	<span class="font-semibold text-gruvbox-fg0">
		
	</span>
</div>

<style>
	img {
		width: 1.5rem;
		height: 1.5rem;
	}
</style>
