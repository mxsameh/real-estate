<script>
  import Footer from "$lib/components/base/Footer.svelte";
  import Header from "$lib/components/base/Header.svelte";
  import Help from "$lib/components/base/Help.svelte";
  import Hero from "$lib/components/home/Hero.svelte";
  import Developers from "$lib/components/home/Developers.svelte";
  import Projects from "$lib/components/home/Projects.svelte";
  import Services from "$lib/components/home/Services.svelte";
</script>

<Header color = {"white"}/>
<Hero/>

<div class="container">
  <Services/>
  <Projects/>
  <Developers/>
  <Help/>
</div>

<Footer/>