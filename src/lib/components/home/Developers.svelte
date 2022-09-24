<script>
  let developers = [
    {img:'./developer1.png', link:'/developer/hassan-allam', id:1},
    {img:'./developer2.png', link:'/developer/emaar', id:2},
    {img:'./developer3.png', link:'/developer/orascom', id:3},
    {img:'./developer4.png', link:'/developer/edge', id:4},
    {img:'./developer1.png', link:'/developer/hassan-allam', id:5},
    {img:'./developer2.png', link:'/developer/emaar', id:6},
    {img:'./developer3.png', link:'/developer/orascom', id:8},
    {img:'./developer4.png', link:'/developer/edge', id:9},
  ]
  let translate = 0;
  let activeDevs = 4;
  let cardLength = 160;
  let space = 80;
  let maxTranslate = (developers.length - activeDevs) * (cardLength + space);
  $: noPrev = translate == 0 ? true : false;
  $: noNext = translate == maxTranslate ? true : false;
  const next = () => {
    if( Math.abs(translate) >= maxTranslate ) return;
    translate -= 240;
  }
  const prev = () => {
    if(noPrev) return;
    translate += 240;
  }
  
</script>

<section class="developers">
  <h2 class="developers__heading">best seller developers</h2>

  <div class="developers__slider">
    <!-- LEFT ARROW -->
    <svg class={noPrev? 'arrow':'arrow arrow--active'} viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg" on:click={prev}>
      <path fill-rule="evenodd" clip-rule="evenodd" d="M37.5 20C37.5 19.6685 37.3683 19.3505 37.1339 19.1161C36.8995 18.8817 36.5816 18.75 36.25 18.75H6.76754L14.635 10.885C14.7513 10.7688 14.8434 10.6308 14.9063 10.479C14.9692 10.3271 15.0016 10.1644 15.0016 9.99999C15.0016 9.83563 14.9692 9.67288 14.9063 9.52103C14.8434 9.36918 14.7513 9.23121 14.635 9.11499C14.5188 8.99877 14.3808 8.90658 14.229 8.84368C14.0771 8.78079 13.9144 8.74841 13.75 8.74841C13.5857 8.74841 13.4229 8.78079 13.2711 8.84368C13.1192 8.90658 12.9813 8.99877 12.865 9.11499L2.86504 19.115C2.74863 19.2311 2.65627 19.369 2.59326 19.5209C2.53024 19.6728 2.4978 19.8356 2.4978 20C2.4978 20.1644 2.53024 20.3272 2.59326 20.4791C2.65627 20.6309 2.74863 20.7689 2.86504 20.885L12.865 30.885C12.9813 31.0012 13.1192 31.0934 13.2711 31.1563C13.4229 31.2192 13.5857 31.2516 13.75 31.2516C13.9144 31.2516 14.0771 31.2192 14.229 31.1563C14.3808 31.0934 14.5188 31.0012 14.635 30.885C14.7513 30.7688 14.8434 30.6308 14.9063 30.479C14.9692 30.3271 15.0016 30.1644 15.0016 30C15.0016 29.8356 14.9692 29.6729 14.9063 29.521C14.8434 29.3692 14.7513 29.2312 14.635 29.115L6.76754 21.25H36.25C36.5816 21.25 36.8995 21.1183 37.1339 20.8839C37.3683 20.6495 37.5 20.3315 37.5 20Z" />
    </svg>

    <!-- DEVELOPERS LIST -->
    <div class="developers__list">
      <ul class="developers__list__wrapper" style={`transform: translateX(${translate}px);`}>

        {#each developers as developer (developer.id) }
          <a class="developer" href={developer.link}>
            <img class="developer__logo" src={developer.img} alt="">
          </a>
        {/each}

      </ul>
    </div>

    <!-- RIGHT ARROW -->
    <svg class={noNext? 'arrow' : 'arrow arrow--active'} viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg" on:click={next}>
      <path fill-rule="evenodd" clip-rule="evenodd" d="M2.4978 20C2.4978 20.3315 2.62949 20.6495 2.86391 20.8839C3.09833 21.1183 3.41628 21.25 3.7478 21.25L33.2303 21.25L25.3628 29.115C25.2466 29.2312 25.1544 29.3692 25.0915 29.521C25.0286 29.6729 24.9962 29.8356 24.9962 30C24.9962 30.1644 25.0286 30.3271 25.0915 30.479C25.1544 30.6308 25.2466 30.7688 25.3628 30.885C25.479 31.0012 25.617 31.0934 25.7688 31.1563C25.9207 31.2192 26.0834 31.2516 26.2478 31.2516C26.4122 31.2516 26.5749 31.2192 26.7268 31.1563C26.8786 31.0934 27.0166 31.0012 27.1328 30.885L37.1328 20.885C37.2492 20.7689 37.3416 20.631 37.4046 20.4791C37.4676 20.3272 37.5 20.1644 37.5 20C37.5 19.8356 37.4676 19.6728 37.4046 19.5209C37.3416 19.3691 37.2492 19.2311 37.1328 19.115L27.1328 9.11501C27.0166 8.99879 26.8786 8.9066 26.7268 8.8437C26.5749 8.7808 26.4122 8.74843 26.2478 8.74843C26.0834 8.74843 25.9207 8.7808 25.7688 8.8437C25.617 8.9066 25.479 8.99879 25.3628 9.11501C25.2466 9.23123 25.1544 9.3692 25.0915 9.52105C25.0286 9.6729 24.9962 9.83565 24.9962 10C24.9962 10.1644 25.0286 10.3271 25.0915 10.479C25.1544 10.6308 25.2466 10.7688 25.3628 10.885L33.2303 18.75L3.7478 18.75C3.41627 18.75 3.09833 18.8817 2.86391 19.1161C2.62949 19.3505 2.4978 19.6685 2.4978 20Z" />
    </svg>

  </div>
</section>

<style lang="scss">
  .developers{
    margin: var(--space-between) auto 0;
    max-width: var(--max-width);


    &__heading{
      font-size: 40px;
      color: var(--gray500);
      text-transform: capitalize;
    }
    &__slider{
      margin-top: 40px;
      align-items: center;
      display: flex;
      justify-content: space-between;
    }
    &__list{
      margin: 0 80px;
      overflow-x: hidden;
      width: calc( 4*160px + 3*80px);

      &__wrapper{
        display: flex;
        align-items: center;
        transition: transform .2s linear;
        gap: 80px;
      } 
    }
  
  }
  
  .developer__logo{
    width: 160px;
  }
  .arrow{
    width: 40px;
    flex-shrink: 0;
    transition: transform .4s linear;
    fill: rgb(150, 150, 150);

    &--active{
      fill: black;
      &:hover{
        cursor: pointer;
        transform: scale(1.1);
      }
    }

  }
  
  @media screen and (max-width: 1023px){
    .arrow{
      display: none;
    }

    .developers__list{
      margin: 0 auto;
      overflow-x: scroll;
      scrollbar-width: none;
    }
  }
  
  @media screen and (max-width: 767px){
    .developers{

      &__heading{
        font-size: 24px;
      }
      &__slider{
        margin-top: 32px;
      }
    }

  }

</style>