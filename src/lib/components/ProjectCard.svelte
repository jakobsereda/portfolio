<script lang="ts">
    let { title, description, image } = $props();
</script>

<div class="bg-gruvbox-fg1 dark:bg-gruvbox-bg1 border border-dashed border-gruvbox-bg4 dark:border-gruvbox-fg4 box-border p-4 gap-4">
    {title}
    {description}
</div>