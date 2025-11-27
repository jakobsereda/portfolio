<script lang="ts">
	let { children } = $props();
</script>

<div class="text-justify text-gruvbox-bg0 dark:text-gruvbox-fg0 text-sm">
	{@render children()}
</div>
