<script lang="ts">
	import ProjectSidebar from '$lib/components/ProjectSidebar.svelte';

	let { children } = $props();
</script>

<div class="p-4 bg-gruvbox-bg2 flex-1 flex flex-row gap-4">
	<div class="w-1/4 border-2 border-gruvbox-blue0 border-solid"> 
		<ProjectSidebar />	
	</div>
	<div class="w-3/4 border-2 border-gruvbox-fg4 border-solid">
		{@render children()}
	</div>
</div>
