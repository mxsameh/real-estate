<script>

  export let location;
  
</script>

<section class="location">
  <h1 class="location__heading title">location</h1>

    <!-- List -->
    <ul class="location__list">
      {#each location.details as info}
      <li class="location__item">{info}</li>
      {/each}
    </ul>

    <!-- Map -->
    <div class="location__map"></div>

</section>

<style lang="scss">
  .location{
    margin-top: 40px;

    &__list{
      margin-top: 24px;
    }
    &__item{
      font-size: 20px;
      line-height: 24px;
      list-style: disc;
      margin-left: 20px;
      color: var(--gray500);
      &:not(:last-child){
        margin-bottom: 8px;
      }
    }
    &__map{
      width: 100%;
      aspect-ratio: 2/1;
      margin-top: 24px;
      background-color: #AAE08F;
      border-radius: 12px;
    }
  }

  @media screen and (min-width:768px){
    .location{
      margin-top: 80px;

      &__list{
        margin-top: 40px;
      }
      &__item{
        font-size: 28px;
        line-height: 32px;
        margin-left: 32px;
        &:not(:last-child){
          margin-bottom: 16px;
        }
      }
      &__map{
        margin: 40px auto;
        max-width: 800px;
      }

    }
  }
  
</style>