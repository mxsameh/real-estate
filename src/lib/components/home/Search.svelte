<script>
  
</script>

<div class="search">
  <form class="search__form">
    <input type="text" name="search-input" class="search__input" id="search-input" placeholder="City, Compound, Developer">
    <button class="search__btn">search</button>
    <button class="search__btn--sm"><img class="search__icon" src="./search-icon.svg" alt="search"></button>
  </form>
</div>

<style lang="scss">

  .search{
    margin: 120px auto 80px;
    padding: 0 var(--page-padding);
    max-width: 1000px;
    width: 100%;

    &__form{
      display: flex;
      align-items: center;
      width: 100%;
      overflow: hidden;
    }
    &__input{
      padding: 13px 24px;
      color: white;
      font-size: 16px;
      border: 2px solid white;
      border-right: none;
      border-radius: 12px 0 0 12px;
      height: 58px;
      width: 80%;
    }
    &__btn{
      background-color: var(--gray800);
      color: white;
      padding: 16px 40px;
      font-size: 24px;
      border-radius:  0 12px 12px 0;
      flex-basis: 15%;
      &:hover{
        background-color: black;
        cursor: pointer;
      }

      &--sm{
        display: none;
        background-color: var(--gray800);
        border-radius: 0 12px 12px 0;
        // flex-basis: 15%;
        width: 20%;
        padding: 8px 16px
      }
    }
    &__icon{
      width: 24px;
      margin: 0 auto;
    }
  }

  @media screen and (max-width:676px){
    .search{
      margin-top: 40px;

      &__input{
        padding: 8px 16px;
        font-size: 16px;
        // flex-shrink: 1;
        // width: 200px;
        height: 44.5px;
      }
      &__btn{
        display: none;
        
        &--sm{
          display: block;
        }
      }

    }
  }
  
</style>