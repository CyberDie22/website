<script lang="ts">
    import Project from "./Project.svelte"

    const project1 = { title: 'This Website', giturl: 'https://github.com/CyberDie22/website', description: 'This is a website for my stuff' }

    const projects = [project1]
</script>

<main>
    {#if projects.length == 0}
        <p>No projects.</p>
    {:else}
        {#each projects as project}
            <!-- <p class=""></p> -->
            <Project title={project.title} description={project.description} giturl={project.giturl} />
        {/each}
    {/if}
</main>