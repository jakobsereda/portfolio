<script lang="ts">
    let { title, description, image } = $props();
</script>

<div class="
    flex flex-col
    bg-gruvbox-fg1 dark:bg-gruvbox-bg1 
    border border-dashed border-gruvbox-bg4 dark:border-gruvbox-fg4 box-border 
    p-4 gap-2 h-full
">
    <img src={image} alt="title" />
    <div class="font-bold text-gruvbox-blue0 dark:text-gruvbox-green1">
        {title}
    </div>
    <div class="text-gruvbox-bg0 dark:text-gruvbox-fg0">
        {description}
    </div>
</div>