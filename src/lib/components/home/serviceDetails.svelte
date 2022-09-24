<script>
  export let service;
</script>

<div class="service">
  <div class="service__logo">
    <img src={service.icon} alt="heart of the capital finance">
  </div>

  <h2 class="service__heading">{service.title}</h2>
  <p class="service__text">{service.text}</p>
  <button class="service__btn">{service.btn}</button>

  <div class="more">
    <span class="more__text">Learn more</span>
    <svg class="more__icon" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg">
      <path d="M13.9725 24.4613C14.0872 24.6278 14.2406 24.764 14.4196 24.8581C14.5986 24.9521 14.7978 25.0013 15 25.0013C15.2022 25.0013 15.4014 24.9521 15.5804 24.8581C15.7594 24.764 15.9128 24.6278 16.0275 24.4613L27.2775 8.21125C27.4077 8.02382 27.4841 7.80429 27.4983 7.57651C27.5125 7.34873 27.464 7.1214 27.3581 6.91924C27.2522 6.71708 27.0929 6.54781 26.8976 6.42982C26.7022 6.31184 26.4782 6.24964 26.25 6.25H3.75001C3.52232 6.25094 3.29919 6.31393 3.10461 6.43221C2.91004 6.55048 2.75139 6.71955 2.64572 6.92124C2.54006 7.12294 2.49137 7.34962 2.5049 7.57692C2.51843 7.80421 2.59366 8.02352 2.72251 8.21125L13.9725 24.4613Z" />
    </svg>
  </div>

</div>


<style lang="scss">

  .service{
    padding: 40px 24px 24px;
    border-radius: 16px;
    flex-basis: 100%;
    max-width: 400px;
    display: flex;
    flex-direction: column;
    position: relative;
    box-shadow: -1px 4px 16px rgba($color: #000000, $alpha: .1);
    transition: transform .2s linear;
    &:hover{
      transform: scale(1.02);
    }

    &__logo{
      background-color: rgba(26, 115, 232, 0.9);
      border-radius: 8px;
      padding: 8px;
      width: fit-content;
      position: absolute;
      top: 0;
      left: 50%;
      transform: translate(-50%,-50%);
      box-shadow: 0px 8px 16px rgba($color: #000000, $alpha: .2);


      img{
        width: 32px;
        display: block;
      }
    }

    &__heading{
      font-size: 24px;
      text-align: center;
    }
    &__text{
      font-size: 16px;
      color: var(--gray500);
      margin-top: 32px;
      text-align: center;
      line-height: 24px;
      margin-bottom: 40px;
    }

    &__btn{
      background-color: var(--blue);
      margin: 0 auto 0;
      margin-top: auto;
      font-size: 20px;
      padding: 12px 32px;
      color: white;
      border-radius: 4px;
      display: block;

      &:hover{
        cursor: pointer;
      background-color: rgb(0, 86, 199);
      }
    }
  }

  .more{
    display: none;
  }

    @media screen and (max-width:767px) {
      .service{
        max-width: none;
        padding: 28px 24px 8px;
        border-radius: 8px;

        &__text, &__btn{
          display: none;
        }
        &__heading{
          font-size: 20px;
        }
        &__logo{
          img{
            width: 24px;
          }
        }
      }

      .more{
        display: flex;
        align-items: center;
        width: fit-content;
        margin: 12px auto 0;

        &__text{
          font-size: 16px;
          color: var(--blue);
        }
        &__icon{
          width: 12px;
          margin-left: 8px;
          fill: var(--blue);
        }
      }


  }

  

</style>