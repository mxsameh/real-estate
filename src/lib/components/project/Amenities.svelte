<script>
  export let amenities;
</script>

<section class="amen">
  <h1 class="amen__title title">amenities</h1>
  <ul class="amen__list">
    {#each amenities as amen }
    <li class="amen__item">
      <img class="amen__img" src={`/${amen.replace(' ','-')}.svg`} alt={amen}>
      <span class="amen__text">{amen}</span>
    </li>
    
    {/each}
  </ul>
</section>


<style lang="scss">
 .amen{
  margin-top: 40px;


  &__list{
    gap: 16px;
    display: grid;
    grid-template-columns: repeat(2, max-content);
    justify-content: space-between;
    max-width: 600px;
    margin: 24px auto 0;
  }
  &__item{
    display: flex;
    gap: 12px;
    align-items: center;
  }
  &__img{
    width: 20px;
  }
  &__text{
    text-transform: capitalize;
    font-size: 16px;
    color: var(--gray500);
  }
 } 

  @media screen and (min-width: 768px){
    .amen{
      margin-top: 80px;

      &__list{
        margin-top: 40px;
        max-height: 180px;
      }
      &__item{
        gap: 16px;
      }
      &__img{
        width:30px;
      }
      &__text{
        font-size: 24px;
      }
    }
  }

  @media screen and (min-width:1024px){
    .amen{
      flex-basis: 45%;

      &__list{
        max-width: 800px;
      }
    }
  }

</style>