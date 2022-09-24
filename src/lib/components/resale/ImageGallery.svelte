<script>
  let img = '/proj1.png'
</script>


<section class="gallery">
  <img class="gallery__img" src={img} alt="">
  <span class="gallery__showall">Show all photos</span>
</section>

<style lang="scss">

  .gallery{
    width:100vw;  
    padding-top:var(--header-height);
    margin-top: 16px;
    position: relative;

    &__img{
      width: 100%;
      aspect-ratio: 3/2;
      display: block;
    }
    &__showall{
      position: absolute;
      bottom: 8px;
      right: 8px;
      font-size: 16px;
      font-weight: 500;
      color: white;
      background-color: rgba($color: #000000, $alpha: .3);
      border-radius: 24px;
      padding: 8px 16px;
    }
  }
  
</style>