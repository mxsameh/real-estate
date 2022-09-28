<script>
  
</script>

<section class="plan">
  <h1 class="plan__title">payment plan</h1>

  <div class="price">
    <h2 class="price__title">property price</h2>
    <input class="price__amount" type="number" placeholder="Enter price">
  </div>

  <div class="loan">
    <h2 class="loan__title">loan duration</h2>
    <ul class="loan__duration">
      <li class="loan__year">2</li>
      <li class="loan__year">3</li>
      <li class="loan__year">4</li>
      <li class="loan__year">5</li>
      <li class="loan__year">6</li>
      <li class="loan__year">7</li>
    </ul>
  </div>

  <div class="down">
    <h2 class="down__title">down payment</h2>
    <ul class="down__payments">
      <li class="down__percent">20 %</li>
      <li class="down__percent">25 %</li>
      <li class="down__percent">30 %</li>
    </ul>
  </div>

  <button class="plan__btn">calculate</button>
</section>

<style lang="scss">
  .plan{
    margin-top: 32px;
    background-color: var(--gray800);
    padding: 24px 16px;
    border-radius: 12px;

    &__title{
      font-size: 24px;
      color: white;
      text-transform: capitalize;
      text-align: center;
    }
    &__btn{
      text-transform: capitalize;
      display: block;
      margin: 40px auto 0;
      font-size: 16px;
      padding: 10px 28px;
      color: white;
      background-color: var(--blue);
      border-radius: 4px;
    }
  }

  .price{
    margin-top: 40px;


    &__title{
      font-size: 16px;
      color: white;
      text-transform: capitalize;
    }
    &__amount{
      font-size: 16px;
      margin-top: 16px;
      color: var(--gray300);
      padding-bottom: 8px;
      border-bottom: 1px var(--gray300) solid;
      width: 100%;
    }


    /* Chrome, Safari, Edge, Opera */
    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }

    /* Firefox */
    input[type=number] {
      -moz-appearance: textfield;
    }
  }

  .loan{
    margin-top: 32px;

    &__title{
      font-size: 16px;
      color: white;
      text-transform: capitalize;
    }
    &__duration{
      margin-top: 16px;
      display: flex;
      align-items: center;
      gap: 16px;
    }
    &__year{
        width: 28px;
        height: 28px;
        border-radius: 50%;
        border: 1px var(--gray300) solid; 
        color: white;
        font-size: 14px;
        display: flex;
        align-items: center;
        justify-content: center;
        line-height: 12px;
        &--active{
          background-color: var(--blue);
          border: 1px var(--blue) solid; 
        }
    }

  }

  .down{
    margin-top: 32px;

    &__title{
      font-size: 16px;
      color: white;
      text-transform: capitalize;
    }
    &__payments{
      display: flex;
      gap: 16px;
      margin-top: 16px;
    }
    &__percent{
      border-radius: 4px;
      padding: 4px 12px;
      border: 1px solid var(--gray300);
      color: white;

      &--active{
      border: 1px solid var(--blue);
      background-color: var(--blue);
      }
    }
  }

</style>