<script>
  
</script>

<section class="unit">
  <h1 class="unit__title">unit details</h1>

  <div class="area">
    <h1 class="area__title unit__heading">area</h1>
    <input class="area__input" type="number" placeholder="Enter unit's area">
  </div>

  <div class="location">
    <h1 class="location__title unit__heading">location</h1>
    <input class="location__input" type="text" placeholder="Write unit's precise location">
  </div>

  <div class="beds">
    <h1 class="beds__title unit__heading">bedrooms</h1>
    <ul class="beds__list">
      <li class="beds__count">1</li>
      <li class="beds__count">2</li>
      <li class="beds__count">3</li>
      <li class="beds__count">4</li>
      <li class="beds__count">5</li>
      <li class="beds__count">6+</li>
    </ul> 
  </div>

  <div class="baths">
    <h1 class="baths__title unit__heading">bedrooms</h1>
    <ul class="baths__list">
      <li class="baths__count">1</li>
      <li class="baths__count">2</li>
      <li class="baths__count">3</li>
      <li class="baths__count">4</li>
      <li class="baths__count">5</li>
      <li class="baths__count">6+</li>
    </ul> 
  </div>

  <div class="condition">
    <h1 class="unit__heading">unit condition</h1>
    <ul class="condition__list">
      <li class="condition__type">core & shell</li>
      <li class="condition__type">not finished</li>
      <li class="condition__type">finished</li>
    </ul>
  </div>

  <div class="type">
    <h1 class="unit__heading">type</h1>
    <select name="type" id="type" class="type__list">
      <option class="type__option" value="apartment">apartment</option>
      <option class="type__option" value="apartment">duplex</option>
      <option class="type__option" value="apartment">penthouse</option>
      <option class="type__option" value="apartment">studio</option>
    </select>
  </div>

  <div class="details">
    <h1 class="unit__heading">unit details</h1>
    <input class="details__input" type="text" placeholder="Write any additional details about your unit">
  </div>

  <button class="unit__review">review</button>

</section>

<style lang="scss">

  .unit{
    margin-top: 40px;
    background-color: var(--gray800);
    border-radius: 16px;
    padding: 32px 16px;
    padding-right: 8px;


    &__title{
      font-size: 20px;
      color: white;
      text-align: center;
      text-transform: capitalize;
    }
    &__heading{
      color:white;
      text-transform: capitalize;
      font-size: 20px;
    }
    &__review{
      display: block;
      margin: 40px auto 0;
      text-transform: capitalize;
      background-color: var(--blue);
      color: white;
      padding: 12px 32px; 
      font-size: 16px;
      border-radius: 4px;
    }
  }

  .area{
    display: flex;
    gap: 24px;
    margin-top: 40px;

    &__input{
      border-bottom: 1px solid var(--gray300);
      font-size: 14px;
      color: var(--gray300);
      padding-bottom: 8px;
      padding-left: 8px;
      width: 100%;
    }
  }
  
  .location{
    margin-top: 32px;

    &__input{
      border-bottom: 1px solid var(--gray300);
      font-size: 14px;
      color: var(--gray300);
      padding-bottom: 8px;
      padding-left: 8px;
      margin-top: 16px;
      width: 100%;
    }
  }
  
  .beds, .baths{
    margin-top: 32px;

    &__list{
      display: flex;
      gap: 12px;
      margin-top: 16px;
    }
    &__count{
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background-color: var(--gray300);
      color: black;
      font-size: 12px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }

  .condition{
    margin-top: 32px;

    &__list{
      margin-top: 16px;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    &__type{
      text-transform: capitalize;
      background-color: var(--gray300);
      color: black;
      font-size: 14px;
      padding: 8px 12px;
      border-radius: 4px;
      white-space: nowrap; 
    }
  }

  .type{
    margin-top: 32px;

    &__list{
      background-color: red;

    }
    &__option{
      font-size: 14px;
      color: white
    }
  }

  .details{
    margin-top: 32px;

    &__input{
      margin-top: 16px;
      padding-bottom: 16px;
      padding-left: 8px;
      border-bottom: 1px solid var(--gray300);
      color: var(--gray300);
      font-size: 14px;
      width:100%;
    }
  }

  
</style>