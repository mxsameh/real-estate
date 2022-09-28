<script>
	import Footer from "$lib/components/base/Footer.svelte";
import Header from "$lib/components/base/Header.svelte";
	import Help from "$lib/components/base/Help.svelte";
	import PaymentPlan from "$lib/components/installments/PaymentPlan.svelte";

  
</script>


<Header />

<div class="container">
  <div class="install">
    <h1 class="install__title">Finance your new home now</h1>
    <p class="install__text">Move now and pay later. we offer a wide varity of loans to buy you dream right now.</p>
  </div>

  <PaymentPlan />

  <div class="customize">
    <h1 class="customize__title">Customize your own payment plan</h1>
    <p class="customize__text">If none of the above payment plans suits you and you need to create your own payment plan please contact us.</p>
  </div>

  <Help />
</div>

<Footer />

<style lang="scss">
  .container{
    padding-top: var(--header-height);
  }
  .install,.customize{
    margin-top: 40px;

    &__title{
      font-size: 24px;
    }
    &__text{
      margin-top: 16px;
      font-size: 16px;
      line-height: 24px;
      color: var(--gray500);
    }
  }
  
  
</style>