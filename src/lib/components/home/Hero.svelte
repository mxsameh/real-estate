<script>
  import Search from "./Search.svelte";

  
</script>

<section class="hero">
  <div class="hero__img"></div>
  <h1 class="hero__heading">find your<br>space now</h1>
  <Search/>
</section>

<style lang="scss">
  
  .hero{
    width: 100%;
    aspect-ratio: 3/2;
    position: relative;
    padding-top: var(--header-height);
    height: 100vh;

    &__img{
      margin-bottom: var(--header-height);
      background:url('/hero-image.png') ;
      height: 100%;
      width:100% ;
      position: absolute;
      z-index: -1;
      top: 0;
      left: 0;
      filter: brightness(.5);
      background-repeat: no-repeat;
      background-position: center;
      background-size: cover;

    }
    &__heading{
      font-size: 96px;
      color: white;
      text-transform: capitalize;
      text-align: center;
      line-height: 1;
      margin-top: 160px;
    }
  }

  @media screen and (max-width:676px){
    .hero{
      height: auto;
      padding-bottom: 80px;
      
      &__heading{
        font-size: 40px;
        margin-top: 80px;
      }
      &__img{
        border-radius: 0 0 12px 12px;
      }

    }
  }

</style>