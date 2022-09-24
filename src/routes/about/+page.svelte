<script>
	import Footer from "$lib/components/base/Footer.svelte";
  import Header from "$lib/components/base/Header.svelte";
	import Help from "$lib/components/base/Help.svelte";

  const members = [
    {id : 1, name : 'ahmed fathy', title : 'CEO / Founder', img : '/member.jpeg'},
    {id : 2, name : 'mahmoud fathy', title : 'Manging Partner', img : '/member.jpeg'},
    {id : 3, name : 'ahmed hesham', title : 'Team Leader', img : '/member.jpeg'},
    {id : 4, name : 'sara mohamed', title : 'Manging Partner', img : '/member.jpeg'},
  ]
</script>

<Header color = {"black"} />

<div class="container">

  <main class="hero">
    <img class="hero__img" src="/white-logo.png" alt="hotc-black-logo">
  </main>

  <section class="who">
    <h1 class="title">who are we</h1>
    <p class="who__text">
      HOTC is a leading company in consulting people on where and why to put their money in a specific area. Our team is customer's oriented, highly-professional, and knowledgeable. They are highly trained to lead a great experience for our clients through all means of professionalism, integrity, and honesty.
      <br>
      HOTC gives specialized financial, investment, and ownership advice to all who are looking to buy a new property from first home, second home, commercial, administrative, and medical.
    </p>
  </section>

  <section class="board">
    <h1 class="board__title title">board of directors</h1>
    <ul class="board__list">
      {#each members as member (member.id) }
      <li class="member">
        <img class="member__img" src={member.img} alt="member's image">
        <h3 class="member__name">{member.name}</h3>
        <p class="member__title">{member.title}</p>
      </li> 
      {/each}
    </ul>
  </section>

  <Help />
</div>

<Footer/>

<style lang="scss">
  .container{
    padding-top: var(--header-height);
  }
  .hero{
    width: 100%;
    padding: 40px 0;
    margin-top: 40px;
    background-color: var(--gray800);
    border-radius: 12px;
    &__img{
      width: 200px;
      margin: 0 auto;
    }
  }

  .who{
    margin-top: 40px;
    &__text{
      font-size: 16px;
      line-height: 24px;
      margin-top: 16px;
      text-align: justify;
    }
  }

  .board{
    margin-top: 40px;

    &__list{
      display: flex;
      align-items: center;
      justify-content: center;
      flex-wrap: wrap;
      gap: 24px;
      margin-top: 16px;
    }
  }

  .member{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    &__img{
      border-radius: 50%;
      width: 100px;
    }
    &__name{
      margin-top: 24px;
      text-transform: capitalize;
      font-size: 16px;
    }
    &__title{
      margin-top: 16px;
      text-transform: capitalize;
      font-size: 16px;
    }
  }

  @media screen and (min-width : 768px){
    .hero{
      margin-top: 80px;
      padding: 56px 0;

      &__img{
        width: 300px;
      }
    }

    .who{
      margin-top: 80px;
      &__text{
        font-size: 24px;
        line-height: 36px;
        margin-top: 40px;
      }
    }

    .board{
      margin-top: 80px;

      &__list{
        margin-top: 40px;
        gap: 80px;
      }
    }

    .member{
      cursor: pointer;

      &:hover &__img{
        filter: grayscale(0);
      }
      &:hover &__name{
          color: var(--blue)
      }

      &__img{
        width: 200px;
        filter: grayscale(1);
      }
      &__name{
        margin-top: 32px;
        font-size: 32px;
      }
      &__title{
        margin-bottom: 24px;
        font-size: 28px;
      }
    }
  }


</style>