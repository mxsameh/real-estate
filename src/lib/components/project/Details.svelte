<script>
  export let details;
</script>

<div class="details">
  <h1 class="details__title title">details</h1>
  <p class="details__text">{details}</p>
</div>



<style lang="scss">

  .details{
    margin-top: 40px;
    
    &__text{
      color: var(--gray500);
      font-size: 16px;
      line-height: 24px;
      margin-top: 24px;
      text-align: justify;
    }
  }

  @media screen and (min-width:768px){
    .details{
      margin-top: 80px;

      &__text{
        font-size: 24px;
        line-height: 36px;
        margin-top: 40px;
      }
    }

  }
  
  @media screen and (min-width:1024px){
    .details{
      max-width: 800px;
      flex-basis: 60%;
    }
  }
</style>