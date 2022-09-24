<script>
import ProjectDetails from "./ProjectDetails.svelte";

  let projects = [
    {id:1, name:'mivida', price:'3,500,000', img:'./proj1.png', url:'/project/mivida'},
    {id:2, name:'hyde park', price:'2,300,000', img:'./proj2.png', url:'/project/hyde-park'},
  ]
  
</script>

<section class="projects">

  <div class="projects__header">
    <h2 class="projects__heading">top projects this month</h2>
    <div class="projects__link">
      <span>View all</span>
      <img src="./r-arrow.svg" alt="">
    </div>
  </div>

  <div class="projects__list">
    {#each projects as project (project.id) }
      <ProjectDetails {project} />
    {/each}
  </div>

</section>

<style lang="scss">
  .projects{
    margin: var(--space-between) auto 0;
    max-width: var(--max-width);

    &__header{
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    &__heading{
      font-size: 40px;
      color: var(--gray500);
      text-transform: capitalize
    }
    &__link{
      display: flex;
      align-items: center;
      gap: 16px;
      span{
        font-size: 24px;
        color: var(--gray500);
      }
      img{
        width:30px;
      }
    }
    &__list{
      display: flex;
      align-items: center;
      gap: 24px;
      margin-top: 40px;
      overflow-x: scroll;
      scrollbar-width: none;
    }

  }

  @media screen and (max-width:676px){
    .projects{
      &__heading{ 
      font-size: 24px;
      }
      &__link{ 
        display: none;
      }
      &__list{
        margin-top: 32px;
      }
    }

  }
  
</style>