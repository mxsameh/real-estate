<script>
  export let project;
</script>

<div class="project">
  <div class="project__img" style={`background-image: url(${project.img});`}></div>

  <div class="project__details" >
    <h3 class="project__name">{project.name}</h3>
    <p class="project__price">Starting Price<span>{project.price} EGP</span></p>
  </div>

</div>

<style lang="scss">
  .project{
    position: relative;
    width: 100%;
    aspect-ratio: 3/2;

    &__name{
      font-size: 32px;
      text-align: center;
      text-transform: capitalize;
      color: white;
    }
    &__price{
      margin-top: auto;
      font-size: 24px;
      color: var(--gray300);
      text-align: center;
      span{
        color: white;
        font-weight: bold;
        display: block;
      }
    }

  }

  .project__img{
    position: absolute;
    top: 0;
    width: 100%;
    filter: brightness(.7);
    aspect-ratio: 3/2;
    background-position: center;
    background-size: cover;
    z-index: -1;
  }
  .project__details{
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 16px 0 8px;
  }

  @media screen and (max-width:676px){
    .project{
      min-width: 220px;
      
      &__img{
        border-radius: 8px;
      }
      &__details{
        padding: 12px 8px 4px;
      }
      &__name{
        font-size: 20px;
        text-align: left;
      }
      &__price{
        font-size: 20px;
        text-align: right;
      }

    }
  }
  
</style>