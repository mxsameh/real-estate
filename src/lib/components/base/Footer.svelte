<footer class="footer">
  <section class="footer__section">

    <div class="details">
      <a href="/">
        <img class="footer__logo" src="/white-logo.png" alt="heart of the capital white logo">
      </a>
      
      <div class="location info">
        <svg class="icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
          <path d="M30 32.5C34.1421 32.5 37.5 29.1421 37.5 25C37.5 20.8579 34.1421 17.5 30 17.5C25.8579 17.5 22.5 20.8579 22.5 25C22.5 29.1421 25.8579 32.5 30 32.5Z"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M30 5C24.6957 5 19.6086 7.10714 15.8579 10.8579C12.1071 14.6086 10 19.6957 10 25C10 29.73 11.005 32.825 13.75 36.25L30 55L46.25 36.25C48.995 32.825 50 29.73 50 25C50 19.6957 47.8929 14.6086 44.1421 10.8579C40.3914 7.10714 35.3043 5 30 5Z" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <p>Block 1177, Building 11, Behind the <br> AAST- Sheraton. Egypt, Cairo Governorate</p>
      </div>

      <div class="phone info">
        <svg class="icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
          <path d="M27.3859 14.6025L18.9284 4.84002C17.9534 3.71502 16.1659 3.72002 15.0334 4.85502L8.07845 11.8225C6.00845 13.895 5.41595 16.9725 6.61345 19.44C13.7675 34.2524 25.7136 46.2152 40.5159 53.39C42.9809 54.5875 46.0559 53.995 48.1259 51.9225L55.1459 44.89C56.2834 43.7525 56.2859 41.955 55.1509 40.98L45.3509 32.5675C44.3259 31.6875 42.7334 31.8025 41.7059 32.8325L38.2959 36.2475C38.1214 36.4305 37.8916 36.5511 37.6418 36.5908C37.3921 36.6306 37.1362 36.5873 36.9134 36.4675C31.3396 33.2578 26.7159 28.6281 23.5134 23.05C23.3935 22.8269 23.3501 22.5706 23.3898 22.3204C23.4296 22.0702 23.5503 21.84 23.7334 21.665L27.1334 18.2625C28.1634 17.2275 28.2759 15.6275 27.3859 14.6V14.6025Z" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <p>(+20) 111 883 6028</p>
      </div>

    </div>

    <div class="category">
      <h2 class="category__heading">top areas</h2>
      <ul class="category__list">
        <li class="category__item">new ciaro</li>
        <li class="category__item">sheikh zayed</li>
        <li class="category__item">north coast</li>
        <li class="category__item">Al-Sokhna</li>
      </ul>
    </div>

    <div class="category">
      <h2 class="category__heading">units</h2>
      <ul class="category__list">
        <li class="category__item">administrative</li>
        <li class="category__item">residential</li>
        <li class="category__item">commercial</li>
        <li class="category__item">coastal</li>
      </ul>
    </div>

    <div class="site-map">
      <a class="site-map__link" href="/about">about us</a>
      <a class="site-map__link" href="/careers">careers</a>
    </div>

  </section>

  <div class="social">
    <h2 class="social__heading">follow us</h2>
    <ul class="social__list">
      <a href="/"><img class="social__icon" src="/fb-icon.svg" alt=""></a>
      <a href="/"><img class="social__icon" src="/ig-icon.svg" alt=""></a>
      <a href="/"><img class="social__icon" src="/twt-icon.svg" alt=""></a>
      <a href="/"><img class="social__icon" src="/yt-icon.svg" alt=""></a>
      <a href="/"><img class="social__icon" src="/in-icon.svg" alt=""></a>
    </ul>
  </div>


</footer>

<style lang="scss">
  $category-margin-top: 32px;
  .footer{
    padding: 24px var(--page-padding) 40px;
    border-radius: 24px 24px 0 0;
    background-color: var(--gray800);
    margin-top: var(--space-between);

    &__logo{
      width: 200px;
    }
    &__section{
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      max-width: var(--max-width);
      margin: 0 auto;
    }
  }

  .location{
    margin-top: 40px;
  }
  .phone{
    margin-top: 24px;
  }

  .info{
    display: block;
    display: flex;
    align-items: center;
    gap: 16px;
    color: white;
  }

  .icon{
    stroke: var(--yellow);
    width: 32px;
    fill: none;
  }
  

  .category{
    margin-top: $category-margin-top;

    &__heading{
      font-size: 24px;
      color: white;
      text-transform: capitalize;
    }
    &__list{
      margin-top: 24px;
      display: flex;
      flex-direction: column;
      gap: 16px;
    }
    &__item{
      font-size: 16px;
      color: var(--gray300);
      text-transform: capitalize;
      width: fit-content;
      &:hover{
        cursor: pointer;
        color: white;
      }
    }

  }

  .site-map{
    display: flex;
    flex-direction: column;
    gap: 32px;
    margin-top: $category-margin-top;

    &__link{
      font-size: 24px;
      text-transform: capitalize;
      font-weight: bold;
      color: var(--gray300);
      text-align: right;
      &:hover{
        cursor: pointer;
        color: white;
      }
    }

  }

  .social{
    margin-top: 32px;

    &__heading{
      text-align: center;
      color: white;
      text-transform: capitalize;
      font-size: 24px;
    }
    &__list{
      display: flex;
      gap: 40px;
      margin: 24px auto 0;
      width:fit-content ;
    }
    &__icon{
      width: 32px; 
    }

  }

  @media screen and (max-width: 1023px){

    .location, .phone{
      display: none;
    }
    .footer{

      &__section{
        flex-wrap: wrap;
      }
      &__logo{
        display: block;
        margin: 0 auto;
      }
    }
    .details{
      flex-basis: 100%;
      margin-bottom: 16px;
    }
    .social{
      margin-top: 40px;
    }

  }

  @media screen and (max-width: 767px){
      
    .footer__logo{
      width: 160px;
    }
      .footer__section{
        flex-direction: column;
        gap: 40px;
      }
      .details{
        margin-bottom: 0;
        width:100%;
        flex-basis: auto;
      }
      .category{
        margin-top: 0;
      }
      .category__list{
        flex-direction: row;
        gap: 32px;
        flex-wrap: wrap;
        row-gap: 16px;
        margin-top: 16px;
      }
      .site-map{
        flex-direction: row;
        gap: 32px;
        margin: 0 auto;
      }
      .social__list{
        gap: 32px
      }

  }


</style>