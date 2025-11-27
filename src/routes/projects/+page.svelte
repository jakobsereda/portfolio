<script lang="ts">
    import ProjectCard from '$lib/components/ProjectCard.svelte';

    const projects = [
        { title: "JavaGotchi", description: "testing testing", image: "./moon.png" },
        { title: "Weisbecker", description: "is anyone there", image: "./sun.png" },
        { title: "Out&About",  description: "424242424242424", image: "./sauropod.png" },
    ];

    function chunk<T>(arr: T[], n: number): T[][] {
        const ret = [];
        for (let i = 0; i < arr.length; i += n) {
            ret.push(arr.slice(i, i + n));
        }
        return ret;
    }

    const rows = chunk(projects, 2);
</script>

<div class="flex flex-col gap-4">
    {#each rows as row}
        <div class="flex flex-row gap-4">
            {#each row as project (project.title)}
                <div class="flex-1 basis-1/2">
                    <ProjectCard 
                        title={project.title}
                        description={project.description}
                        image={project.image}
                    />
                </div>
            {/each}
        </div>
    {/each}
</div>