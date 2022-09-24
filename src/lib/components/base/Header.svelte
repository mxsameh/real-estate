<script>
  let isOpened = false
  const toggleMenu = () => {
    isOpened = !isOpened;
    // console.log( 'Is menu opened ?', isOpened );
  }
  export let color = 'black';

</script>

<header class="header">
  <div class="header__wrapper">

    <a href="/" class="logo">
      <img class="logo__img" src={`/${color}-logo.png`} alt="heart of the capital logo">
    </a>

    <nav class="nav">
      <ul class="nav__list">
        <a class="nav__link" href="/">home</a>
        <a class="nav__link" href="/projects">projects</a>
        <a class="nav__link" href="/developers">developers</a>
        <a class="nav__link" href="/resale">resale</a>
      </ul>
      <button class="nav__btn">buy home</button>
    </nav>

    <svg class="menu__icon" viewBox="0 0 80 80" xmlns="http://www.w3.org/2000/svg" on:click={toggleMenu}>
      <path d="M73.3334 60.0166C73.3334 61.85 71.8467 63.3333 70.0167 63.3333H43.3167C42.4371 63.3333 41.5935 62.9839 40.9715 62.3619C40.3495 61.7399 40 60.8963 40 60.0166C40 59.137 40.3495 58.2934 40.9715 57.6714C41.5935 57.0494 42.4371 56.7 43.3167 56.7H70.0167C71.85 56.7 73.3334 58.1833 73.3334 60.0166V60.0166ZM73.3334 40C73.3334 41.8333 71.8467 43.3166 70.0167 43.3166H9.98335C9.10372 43.3166 8.26011 42.9672 7.63812 42.3452C7.01612 41.7232 6.66669 40.8796 6.66669 40C6.66669 39.1203 7.01612 38.2767 7.63812 37.6547C8.26011 37.0327 9.10372 36.6833 9.98335 36.6833H70.0167C71.85 36.6833 73.3334 38.17 73.3334 40V40ZM70.0167 23.3C70.8963 23.3 71.7399 22.9505 72.3619 22.3285C72.9839 21.7065 73.3334 20.8629 73.3334 19.9833C73.3334 19.1037 72.9839 18.2601 72.3619 17.6381C71.7399 17.0161 70.8963 16.6666 70.0167 16.6666H29.9834C29.5478 16.6666 29.1165 16.7524 28.7141 16.9191C28.3117 17.0858 27.9461 17.3301 27.6381 17.6381C27.3301 17.946 27.0858 18.3117 26.9192 18.7141C26.7525 19.1165 26.6667 19.5477 26.6667 19.9833C26.6667 20.4188 26.7525 20.8501 26.9192 21.2525C27.0858 21.6549 27.3301 22.0206 27.6381 22.3285C27.9461 22.6365 28.3117 22.8808 28.7141 23.0475C29.1165 23.2142 29.5478 23.3 29.9834 23.3H70.0167Z" fill={color}/>
    </svg>


  </div>
</header>

<style lang="scss">
  .header{
    width: 100%;
    position: absolute;
    top: 0;
    padding: 8px var(--page-padding) 0;
    z-index: 1;
    color: black;

    &__wrapper{
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: var(--max-width);
      margin: 0 auto;
    }
  }
  .logo{
    width: 160px;
     &__img{
      width: 100%;
     }
  }

  .nav{
    display: flex;
    align-items: center;
    &__list{
      display: flex;
      gap: 32px;
    }
    &__link{
      font-size: 20px;
      text-transform: capitalize;
    }

    &__btn{
      text-transform: capitalize;
      font-size: 16px;
      color: white;
      background-color: var(--blue);
      padding: 8px 24px;
      border-radius: 4px;
      margin-left: 40px;

      &:hover{
        cursor: pointer;
        background-color: rgba($color: #1A73E8, $alpha: .8);
        color: black;
      }
    }

  }

  .menu__icon{
    display: none;
    width: 40px;

    &:hover{
      cursor: pointer;
    }
  }


  // Tablet Breakpoint
  @media screen and (max-width: 1023px){
    .header{
      padding: 16px var(--page-padding) 0;
    }
    .logo{
      width: 120px;
    }
    .nav{
      display: none;
    }
    .menu__icon{
      display: block;
    }


  }

  
</style>