<script lang="ts">
    import ProjectCard from '$lib/components/ProjectCard.svelte';

    const projects = [
        { title: "JavaGotchi", description: "testing testing testing testing", image: "./moon.png" },
        { title: "Weisbecker", description: "is anyone there", image: "./sun.png" },
        { title: "Out&About",  description: "424242424242424", image: "./sauropod.png" },
    ];
</script>

<div class="grid grid-cols-2 gap-4">
    {#each projects as project (project.title)}
        <div class="flex-1 basis-1/2">
            <ProjectCard 
                title={project.title}
                description={project.description}
                image={project.image}
            />
        </div>
    {/each}
</div>