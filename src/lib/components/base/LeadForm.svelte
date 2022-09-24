<script>
  
</script>

<div class="lead">
  <h2 class="lead__heading">Want help finding the place that fits you ?</h2>
  <p class="lead__text">Fill thr form below and our proffesional property consultans will get in touch with you within a few hours</p>

  <form class="lead__form">
    <label for="name">name</label>
    <input type="text" id="name" placeholder="Enter Your Name">

    <label for="phone">phone</label>
    <input type="text" id="phone" placeholder="Enter Your Number">

    <button class="form__btn">Request a call</button>
  </form>

</div>

<style lang="scss">
 .lead{
  padding: 32px 24px;
  flex-basis: 60%;

  &__heading{
    font-size: 32px;
  }
  &__text{
    font-size: 20px;
    color: var(--gray500);
    margin-top: 16px;
    max-width: 620px;
  }
  &__form{
    margin-top: 48px;
  }

 } 

  label{
    display: block;
    text-transform: capitalize;
    margin-bottom: 16px;
    font-weight: bold;
    color: var(--gray500);
    font-size: 24px;
  }
  input{
    font-size: 20px;
    padding:0 0 8px 8px;
    border-bottom: 1px solid var(--gray500);
    width: 100%;
  }
  #name{
    margin-bottom: 32px;
  }

  .form__btn{
    font-size: 24px;
    background-color: var(--blue);
    padding: 12px 32px;
    color: white;
    border-radius: 4px;
    display: block;
    margin-top: 48px;
  }

  @media screen and (max-width:1023px){
    .lead{
      border-radius: 12px;
      background-color: var(--gray100);
      flex-basis: auto;
      padding: 32px 40px;
      width: 100%;

      &__heading{
        white-space: nowrap;
      }
      &__text{
        max-width: none;
      }
    }

    .form__btn{
      margin: 48px auto 0;
    }

  }

  @media screen and (max-width:767px){
    .lead{
      order: 2;
      padding: 32px 24px;

      &__heading{
        white-space: normal;
        font-size: 24px;
      }
      &__text{
        font-size: 16px;
        margin-top: 8px;
      }
    }

    .lead__form{
      margin-top: 24px;

      label{
        font-size: 20px;
      }
      input{
        font-size: 16px;
      }
    }

    .form__btn{
        font-size: 20px;
        margin: 32px auto 0;
        padding: 12px 24px;
      }

  }

</style>