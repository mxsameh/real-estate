<script>
	import Footer from "$lib/components/base/Footer.svelte";
import Header from "$lib/components/base/Header.svelte";
	import Help from "$lib/components/base/Help.svelte";
	import UnitDetails from "$lib/components/pricing/UnitDetails.svelte";

  
</script>

<Header />

<div class="container">
  <main class="pricing">
    <h1 class="pricing__title">Know your property's worth in market</h1>
    <p class="pricing__text">Review your property with our proffesional property consultant to know much does it worth in the market</p>
  </main>

  <UnitDetails />

  <Help />

</div>

<Footer />


<style lang="scss">
  .container{
    padding-top:var(--header-height);
  }

  .pricing{
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