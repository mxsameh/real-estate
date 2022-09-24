<script>
  
</script>

<section class="column">

  <button class="save__btn">Save in list</button>

  <div class="contact">
    <button class="call contact__btn">call</button>
    <button class="whats contact__btn">whatsapp</button>
  </div>

  <form class="form">
    <h2 class="form__heading">for more details</h2>
    <label class="form__label" for="name">name</label>
    <input class="form__input" type="text" id="name" placeholder="Enter Your Name">
    
    <label class="form__label" for="name">phone</label>
    <input class="form__input" type="text" id="phone" placeholder="Enter Your Number">

    <label class="form__label" for="name">message</label>
    <input class="form__input" type="text" id="message" placeholder="Write Message">

    <button class="form__btn">send</button>

  </form>

</section>

<style lang="scss">
  .column{
    display: none;
  }

  @media screen and (min-width: 1024px){
    .column{
      display: block;
      align-self: flex-start;
      position: sticky;
      top: 0;
    }
  }

  
  .save__btn{
    width: 100%;
    border: 2px solid black;
    border-radius: 8px;
    text-align: center;
    padding: 12px 32px;
    font-size: 16px;

    &:hover{
      color: white;
      background-color: rgb(255, 95, 95);
      border: 2px solid rgb(255, 95, 95);
      cursor: pointer;

    }
  }

  .contact{
    display: flex;
    align-items: center;
    gap: 20px;
    widows: 100%;
    margin-top: 24px;

    &__btn{
      color: white;
      background-color: black;
      font-size: 16px;
      flex-basis: 50%;
      padding: 12px 32px;
      border-radius: 8px;
      text-transform: capitalize;

      &:hover{
        cursor: pointer;
        background-color: limegreen;
      }
    }
    
  }

  .form{
    width: 100%;
    background-color: var(--gray100);
    padding: 24px 16px;
    margin-top: 40px;
    border-radius: 12px;

    &__heading{
      text-transform: capitalize;
      font-size: 24px;
      text-align: center;
      margin-bottom: 16px;
    }
    &__label{
      display: block;
      font-size: 16px;
      text-transform: capitalize;
      margin-top: 24px;
      color: var(--gray500);
      font-weight: bold;
    }
    &__input{
      border-bottom: 1px solid var(--gray500);
      padding: 0 8px 8px;
      margin-top: 16px;
      width: 100%;
    }
    &__btn{
      color: white;
      background-color: var(--blue);
      padding: 8px 40px;
      width: 50%;
      margin:24px auto 0;
      display: block;
      font-size: 20px;
      border-radius: 8px;
      text-transform: capitalize;

      &:hover{
        cursor: pointer;
        background-color: #00459e;
      }
    }

  }

  #message{
    padding: 0 12px 8px;

  }


  
</style>