<script lang="ts">

  let notNumerError = false;
  const formatNumber = (e : any) =>
  {
    let value = e.target.value
    const regex = /^[0-9]+$/
    const lastChar = value.slice(-1)

    // If a letter is pressed
    if(!lastChar.match(regex))
    {
      notNumerError = true
      console.log( 'please enter a number' );
      e.target.value = value.slice(0,-1)
      return
    }

    notNumerError = false;
    // Change value to number
    value = value.replaceAll(',','')
    const number = parseInt(value)

    // Check if number
    if(!Number.isNaN(number))
    {
      // Format number with commas
      let formatedNumber = number.toLocaleString()
      e.target.value = formatedNumber;
    }

  }
  

  // Loan
  const loanYears = [2,3,4,5,6,7]
  let selectedLoanYear : number;
  const selectLoanYear = (e: any) =>
{
  selectedLoanYear = parseInt(e.target.innerText)
}

// Down Payment
const downPayments = [20,25,30]
  let selectedDownPayment : number;
  const selectDownPayment = (e: any) =>
{
  selectedDownPayment = parseInt(e.target.innerText)
}
</script>

<section class="plan">
  <h1 class="plan__title">payment plan</h1>

  <div class="price">
    <h2 class="price__title">property price</h2>
    <input class="price__amount" type="text" placeholder="Enter price" on:keyup={formatNumber}>
    {#if notNumerError}
    <p class="price__error">* Please enter a number</p>
    {/if}
  </div>

  <div class="loan">
    <h2 class="loan__title">loan duration</h2>
    <ul class="loan__duration">
      {#each loanYears as loanYear,i }
      <li class={selectedLoanYear == loanYear ? "loan__year loan__year--active":"loan__year"} on:click={selectLoanYear}>{loanYear}{#if i == loanYears.length-1}+{/if}</li>
      {/each}
    </ul>
  </div>

  <div class="down">
    <h2 class="down__title">down payment</h2>
    <ul class="down__payments">
      {#each downPayments as downPayment }
      <li class={selectedDownPayment == downPayment ? "down__percent down__percent--active" : "down__percent"} on:click={selectDownPayment}>{downPayment} %</li>
      {/each}
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
    &__error{
      font-size: 12px;
      margin-top: 8px;
      color: rgb(255, 40, 40);
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
        width: 32px;
        height: 32px;
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
          color: white;
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