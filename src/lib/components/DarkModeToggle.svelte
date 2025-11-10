<script lang="ts">
    import { onMount } from 'svelte';

    let is_dark = false;

    onMount(() => {
		is_dark = document.documentElement.classList.contains("dark");
	});

	function toggle_dark_mode() {
		is_dark = !is_dark;
		if (is_dark) {
			document.documentElement.classList.add("dark");
			localStorage.setItem("theme", "dark");
		} else {
			document.documentElement.classList.remove("dark");
			localStorage.setItem("theme", "light");
		}
	}
</script>

<button on:click={toggle_dark_mode} aria-label="toggle-dark-mode" class="cursor-pointer transition hover:scale-105">
{#if is_dark}
    <img src="/sun.png" alt="sun" class="h-[1em] w-[1em]" />
{:else}
    <img src="/moon.png" alt="moon" class="h-[1em] w-[1em]" />
{/if}
</button>
