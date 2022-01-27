<script lang="ts">
    export let title;
    export let description;
    export let giturl = "";

    export let klass = "";
</script>

<main class="p-3">
    <div class="{klass} flex flex-col w-fit bg-sky-800 rounded-lg">
        <h3 class="p-3" >{title}</h3>
        {#if giturl !== ""}
            <a class="p-3 underline" href={giturl}>Git</a>
        {/if}
        <p class="p-3" >{description}</p>
    </div>
</main>