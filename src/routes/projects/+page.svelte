<script lang="ts">
    import ProjectCard from '$lib/components/ProjectCard.svelte';
    import UnderConstruction from '$lib/components/UnderConstruction.svelte';

    const projects = [
        { title: "Gander",
          description: "A functional, compiled programming language with a small but powerful syntax",
          image: "" },
        { title: "8-Bit CPU",
          description: "A physical CPU built using simple logic gates and breadboards",
          image: "" },
        { title: "Out&About", 
          description: "A web app that cultivates community, built during nwHacks 2025", 
          image: "" },
        { title: "Weisbecker", 
          description: "A CHIP-8 interpreter built with Rust", 
          image: "" },
        { title: "JavaGotchi", 
          description: "A desktop game where you train a team of pets to compete in a sports tournament", 
          image: "" },
        { title: "NBA Classifier",
          description: "A KNN model that predicts the position an NBA player is most suited for",
          image: "" },
    ];
</script>

<div class="grid grid-cols-2 gap-4">
    {#each projects as project (project.title)}
        <!-- <ProjectCard 
            title={project.title}
            description={project.description}
            image={project.image}
        /> -->
    {/each}
    <UnderConstruction />
</div>