<script>
import ServiceDetails from "./serviceDetails.svelte";

  let services = [
    {
      id:1,
      icon:'./finance-icon.svg',
      title:'Finance your home',
      text:`Don't have the cash to buy a new home we will home you buy it now and pay later. `,
      btn:'Start now'
    },
    {
      id:2,
      icon:'./deals-icon.svg',
      title:'Hot deals properties',
      text:`Check a huge collection of awsome properties with below market prices.`,
      btn:'View all'
    },
    {
      id:3,
      icon:'./review-icon.svg',
      title:'Review your property',
      text:`Know exactly how much does your property worth in the market today.`,
      btn:'Review now'
    },
  ]
</script>


<section class="services">
  <h2 class="services__heading">our services</h2>

 <div class="services__list">
  {#each services as service (service.id) }
    <ServiceDetails {service}/>
  {/each}
 </div> 

</section>


<style lang="scss">
  .services{
    margin-top: 80px;

    &__heading{
      font-size: 40px;
      text-align: center;
      text-transform: capitalize;
    }
    &__list{
      display: flex;
      gap: 20px;
      row-gap: 48px;
      width: fit-content;
      margin: 80px auto 0;
    }
  }

  @media screen and (max-width: 1023px){
    .services{
      margin-top: 40px;

      &__list{
        // flex-direction: column;
        flex-wrap: wrap;
        margin: 64px auto 0;
      }
    }

  }

  @media screen and (max-width: 767px){
    .services{
      flex-direction: column;
      gap: 40px;
      margin: 40px 0 40px;
      width: 100%;

      &__heading{
        font-size: 28px;
      }
      &__list{
        flex-direction: column;
        width: 100%;
      }
    }

  }
  
</style>