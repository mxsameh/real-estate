<script>
import Project from "./Project.svelte";


  export let projects;
</script>

<div class="projects">
  <h1 class="projects__heading title">similar projects</h1>

  <div class="projects__list">
    {#each projects as project (project.id) }
      <Project {project} />
    {/each}
  </div>

</div>

<style lang="scss">
  .projects{
    margin-top: 40px;

    &__list{
      margin: 24px auto 0;
      display: flex;
      gap: 16px;
      overflow-x:scroll ;
      scrollbar-width: none;
      width: fit-content;
      max-width: 100%;

    }
  }

  @media screen and (min-width: 768px){
    .projects{
      margin-top: 80px;

      &__list{
        margin-top: 40px;
      }
    }
  }
  
</style>