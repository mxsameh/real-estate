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
      aspect-ratio: 3/2;
      border-radius: 8px;
      min-width: 240px;
      // width: 100%;
      flex-shrink: 0;
      width: calc((100vw - 80px) * (80/100));
      max-width: 400px;

      
      &__img{
        position: absolute;
        top: 0;
        width: 100%;
        aspect-ratio: 3/2;
        border-radius: 8px;
        filter: brightness(.7);
        background-position: center;
        background-size: cover;
        z-index: -1;
      }
      &__details{
        display: flex;
        flex-direction: column;
        height: 100%;
        padding: 12px 8px 4px;
      }
      &__name{
        font-size: 20px;
        text-transform: capitalize;
        color: white;

      }
      &__price{
        margin-top: auto;
        font-size: 20px;
        color: var(--gray300);
        text-align: right;
        span{
          color: white;
          font-weight: bold;
          display: block;
        }
      }

    }
    @media screen and (min-width:768px){
      .project{
        border-radius: 16px;
        max-width: 400px;

        &__details{
          padding: 16px 0 8px;
        }
        &__name{
          font-size: 28px;
          text-align: center;
        }
        &__price{
          text-align: center;
          font-weight: bold;
          span{
            margin-top: 4px;
          }
        }

      }
    }

</style>