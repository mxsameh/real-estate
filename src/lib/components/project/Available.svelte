<script>
  import UnitCard from "./UnitCard.svelte";

  export let properties;

  let activeTab = 'apartments';
  let units = properties.apartments;

  const select = (e) =>
  {
    let tabs = document.querySelectorAll('.units__type');

    tabs.forEach(tab => {
      tab.classList.remove('units__type--active')
    })

    e.target.classList.add('units__type--active')

    activeTab = e.target.dataset.tab;

    switch (e.target.dataset.tab){
      case 'apartments':
        units = properties.apartments;
        break;
      case 'villas':
        units = properties.villas;
        break;
      case 'others':
        units = properties.others;
        break;
      default:
        units = properties.apartments;
        break;
    }
  }

  
</script>

<section class="units">
  <h1 class="units__title title">available units</h1>

  <div class="units__wrapper">

    <nav class="units__nav">
      <span data-tab="apartments" class='units__type units__type--active' on:click={select}> apartments</span>
      <span data-tab="villas" class="units__type" on:click={select}>villas</span>
      <span data-tab="others" class="units__type" on:click={select}>others</span>
    </nav>

    <div class="units__list">
      <div class="list__wrapper">
        {#if units }
          {#each units as unit (unit.id) }
            <UnitCard {unit} />
          {/each}
        {/if}
      </div>
    </div>


  </div>

</section>

<style lang="scss">
  .units{
    margin-top: 40px;

    &__wrapper{
      margin-top: 24px;
      border-radius: 12px;
    }
    &__nav{
      display: flex;
      gap: 24px;
      width: fit-content;
      margin: 0 auto;
    }
    &__type{
      color: var(--gray500);
      font-weight: 500;
      text-transform: capitalize;
      padding-bottom: 4px;
      font-size: 16px;
      &--active{
        color:black;
        border-bottom: 1px solid black ;
      }
    }
    
    &__list{
      margin-top: 24px;
      width: 100%;
      overflow: scroll;
      scrollbar-width: none;
    }
    
  }

  .list__wrapper{
    display: flex;
    gap: 24px;
    width: fit-content;
    margin: 0 auto;
  }
  
  @media screen and (min-width: 768px){
    .units{
      margin-top: 80px;

      &__wrapper{
        margin-top: 40px;
      }
      &__nav{
        gap: 40px;
      }
      &__type{
        font-size: 24px;
      }
      &__list{
        margin-top: 40px;
      }


    }
  }

</style>