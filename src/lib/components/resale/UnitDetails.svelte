<script>
  let location = 'mivida - new cairo';
  let type = 'villa - standalone';
  let beds = 5;
  let baths = 4;
  let area = 420;
  let price = 5000000;
</script>

<section class="unit__info">

  <div class="details">
  <!-- LOCATION -->
  <div class="details__location">
    <svg class="details__icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
      <path d="M30 32.5C34.1421 32.5 37.5 29.1421 37.5 25C37.5 20.8579 34.1421 17.5 30 17.5C25.8579 17.5 22.5 20.8579 22.5 25C22.5 29.1421 25.8579 32.5 30 32.5Z"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M30 5C24.6957 5 19.6086 7.10714 15.8579 10.8579C12.1071 14.6086 10 19.6957 10 25C10 29.73 11.005 32.825 13.75 36.25L30 55L46.25 36.25C48.995 32.825 50 29.73 50 25C50 19.6957 47.8929 14.6086 44.1421 10.8579C40.3914 7.10714 35.3043 5 30 5Z" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    <span class="details__text">{location}</span>
  </div>
  <!-- TYPE -->
  <div class="details__type">
    <svg class="details__icon" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
      <path d="M33.3333 31.6667V17.5C33.3333 17.2413 33.2731 16.9861 33.1573 16.7547C33.0416 16.5233 32.8736 16.322 32.6666 16.1667L21 7.41671C20.7115 7.20034 20.3606 7.08337 20 7.08337C19.6393 7.08337 19.2885 7.20034 19 7.41671L7.33329 16.1667C7.1263 16.322 6.95829 16.5233 6.84258 16.7547C6.72687 16.9861 6.66663 17.2413 6.66663 17.5V31.6667C6.66663 32.1087 6.84222 32.5327 7.15478 32.8452C7.46734 33.1578 7.89127 33.3334 8.33329 33.3334H31.6666C32.1087 33.3334 32.5326 33.1578 32.8451 32.8452C33.1577 32.5327 33.3333 32.1087 33.3333 31.6667Z" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    <span class="details__text">{type}</span>
  </div>

  </div>

  <div class="unit__facts">

    <!-- PRICE -->
    <div class="fact">
      <span class="fact__heading">price</span>
      <span class="fact__text">{price.toLocaleString()} EGP</span>
    </div>
    <span class="line"></span>
    <!-- BEDROOMS -->
    <div class="fact">
      <span class="fact__heading">bedrooms</span>
      <span class="fact__text">{beds} Bedrooms</span>
    </div>
    <span class="line"></span>
    <!-- AREA -->
    <div class="fact">
      <span class="fact__heading">area</span>
      <span class="fact__text">{area} sqm</span>
    </div>
    <span class="line"></span>
    <!-- BATHROOMS -->
    <div class="fact">
      <span class="fact__heading">bathrooms</span>
      <span class="fact__text">{baths} Bathrooms</span>
    </div>

  </div>

</section>

<style lang="scss">
  .unit__info{
    max-width: 500px;
    margin: 0 auto;
  }
  .details{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 16px;

    &__location, &__type{
      display: flex;
      align-items: center;
      gap: 8px;
    }
    &__location{
      margin-right: 40px;
    }

    &__icon{
      width:28px;
      fill:none;
      stroke:black;
      flex-shrink: 0;
    }
    &__text{
      font-size: 20px;
      font-weight: 500;
      text-transform: capitalize;
    }
  }

  .unit__facts{
    background-color: var(--gray100);
    border-radius: 12px;
    padding: 16px 24px;
    // display: flex;
    // justify-content: space-between;
    margin-top: 24px;

    display: grid;
    grid-template-columns: repeat(2, max-content);
    justify-content: space-between;
    gap: 16px;
  }
  .line{
    display: none;
  }
  .fact{
    display: flex;
    flex-direction: column;
    gap: 8px;

    &__heading{
      font-size: 20px;
      text-transform: capitalize;
    }
    &__text{
      font-weight: bold;
      font-size: 20px;
    }
  }

  @media screen and (min-width: 768px) {
    .unit__info{
      max-width: none;

    }
    .details{
      flex-direction: row;
      justify-content: space-between;
      align-items: center;

      &__icon{
        width: 32px;
      }
      &__text{
        font-size: 24px;
      }
    }

    .unit__facts{
      padding: 16px;
      border-radius: 12px;
      border: 2px solid var(--gray300);
      background-color: transparent;
      // justify-content: flex-start;
      grid-template-columns: repeat(7,max-content);
    }

    .line{
      display: block;
      height: 100%;
      border: 1px solid var(--gray300);
    }

  }
  
</style>