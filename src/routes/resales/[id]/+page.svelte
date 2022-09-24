<script>
import Header from "$lib/components/base/Header.svelte";
import Help from "$lib/components/base/Help.svelte";
import Footer from "$lib/components/base/Footer.svelte";
import SimilarProperties from "$lib/components/resale/SimilarProperties.svelte";
import Payment from "$lib/components/resale/Payment.svelte";
import UnitDetails from "$lib/components/resale/UnitDetails.svelte";
import ImageGallery from "$lib/components/resale/ImageGallery.svelte";
import Contact from "$lib/components/resale/Contact.svelte";

let unit = {
  img:'/p1.png',
  location: 'mivida - new cairo',
  type: 'villa - standalone',
  price: 5000000,
  area: 420,
  beds: 5,
  baths: 4
}
  
</script>

<Header/>
<ImageGallery />
<div class="container">
  <main class="main">
    <div class="wrapper">
      <UnitDetails/>
      <Payment price = {unit.price}/>
    </div>
    <Contact />
  </main>
  <SimilarProperties />
  <Help />
</div>

<Footer/>


<style>
  .container{
    max-width: var(--max-width);
    margin: 0 auto;
  }
  .main{
    margin-top: 40px;
  }
  @media screen and (min-width: 1024px){
    .main{
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 24px;
    }

  }
  
</style>