<script>
  import Contact from "$lib/components/base/Contact.svelte";
  import LeadForm from "$lib/components/base/LeadForm.svelte";
  
</script>

<section class="help">
  <LeadForm/>
  <Contact/>
</section>

<style>
  .help{
    display: flex;
    border-radius: 16px;
    padding: 16px;
    background-color: var(--gray100);
    align-items: flex-start;
    width: 100%;
    max-width: var(--max-width);
    margin: var(--space-between) auto 0;
    justify-content: space-between;
  }

  /* TABLET SIZE   */
  @media screen and (max-width: 1023px){
    .help{
      flex-direction: column;
      background-color: transparent;
      padding: 0;
    }
  }

  @media screen and (max-width: 640px){
    .help{
      gap: 24px;
    }
  }
  
</style>