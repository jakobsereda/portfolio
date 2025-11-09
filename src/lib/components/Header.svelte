<script lang="ts">
	import { page } from "$app/state";

	const items = [
		{ route: '/',         label: 'Home'     },
		{ route: '/projects', label: 'Projects' },
		{ route: '/blog',     label: 'Blog'     },
		{ route: '/music',    label: 'Music'    },
	];
</script>

<div class="flex flex-col">
	<div class="flex flex-row justify-between items-end">
		<span class="font-semibold text-3xl text-gruvbox-bg0 dark:text-gruvbox-fg0">
			Jakob's <span class="text-gruvbox-blue0 dark:text-gruvbox-green1">Website</span>
		</span>
		<div class="flex gap-8 justify-end">
		{#each items as item (item.route)}
			<a href={item.route} class="font-semibold {page.url.pathname === item.route ? 'text-gruvbox-bg0 dark:text-gruvbox-fg0' : 'text-gruvbox-fg4 dark:text-gruvbox-bg4'}">
				{item.label}
			</a>
		{/each}
		</div>
	</div>
	<hr class="mt-2 border-dashed text-gruvbox-fg4 dark:text-gruvbox-bg4" />
</div>

<style>
	a {
		transition: transform 0.2s ease;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
