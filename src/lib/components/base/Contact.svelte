<div class="contact">
  <h2 class="contact__heading">contact us</h2>
  <p class="contact__text contact__details">Whenever you need us we'll be there for you. Our professional team is always available for help.</p>

    <div class="contact__info">
      <!-- PHONE -->
      <div class="phone">
        <svg class="phone-icon contact__icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
          <path d="M27.3859 14.6025L18.9284 4.84002C17.9534 3.71502 16.1659 3.72002 15.0334 4.85502L8.07845 11.8225C6.00845 13.895 5.41595 16.9725 6.61345 19.44C13.7675 34.2524 25.7136 46.2152 40.5159 53.39C42.9809 54.5875 46.0559 53.995 48.1259 51.9225L55.1459 44.89C56.2834 43.7525 56.2859 41.955 55.1509 40.98L45.3509 32.5675C44.3259 31.6875 42.7334 31.8025 41.7059 32.8325L38.2959 36.2475C38.1214 36.4305 37.8916 36.5511 37.6418 36.5908C37.3921 36.6306 37.1362 36.5873 36.9134 36.4675C31.3396 33.2578 26.7159 28.6281 23.5134 23.05C23.3935 22.8269 23.3501 22.5706 23.3898 22.3204C23.4296 22.0702 23.5503 21.84 23.7334 21.665L27.1334 18.2625C28.1634 17.2275 28.2759 15.6275 27.3859 14.6V14.6025Z" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <p class="contact__text">(+20) 111 883 6028</p>
      </div>

      <!-- LOCATION -->
      <div class="location">
        <svg class="location-icon contact__icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
          <path d="M30 32.5C34.1421 32.5 37.5 29.1421 37.5 25C37.5 20.8579 34.1421 17.5 30 17.5C25.8579 17.5 22.5 20.8579 22.5 25C22.5 29.1421 25.8579 32.5 30 32.5Z"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M30 5C24.6957 5 19.6086 7.10714 15.8579 10.8579C12.1071 14.6086 10 19.6957 10 25C10 29.73 11.005 32.825 13.75 36.25L30 55L46.25 36.25C48.995 32.825 50 29.73 50 25C50 19.6957 47.8929 14.6086 44.1421 10.8579C40.3914 7.10714 35.3043 5 30 5Z" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <p class="contact__text">Block 1177, Building 11, Behind the AAST- Sheraton. Egypt, Cairo Governorate</p>
      </div>

      <!-- LOCATION -->
      <div class="email">
        <svg class="email-icon contact__icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
          <path d="M52.5 11.25H7.5C6.50544 11.25 5.55161 11.6451 4.84835 12.3483C4.14509 13.0516 3.75 14.0054 3.75 15V45C3.75 45.9946 4.14509 46.9484 4.84835 47.6516C5.55161 48.3549 6.50544 48.75 7.5 48.75H52.5C53.4946 48.75 54.4484 48.3549 55.1516 47.6516C55.8549 46.9484 56.25 45.9946 56.25 45V15C56.25 14.0054 55.8549 13.0516 55.1516 12.3483C54.4484 11.6451 53.4946 11.25 52.5 11.25V11.25ZM48.375 15L30 27.7125L11.625 15H48.375ZM7.5 45V16.7062L28.9313 31.5375C29.2451 31.7552 29.618 31.8719 30 31.8719C30.382 31.8719 30.7549 31.7552 31.0687 31.5375L52.5 16.7062V45H7.5Z"/>
        </svg>
        <p class="contact__text">Support@heartofthecapital.com</p>
      </div>

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
      

    </div>

</div>


<style lang="scss">
  .contact{
    color: white;
    background-color: var(--gray800);
    padding: 32px;
    border-radius: 12px;
    max-width: 460px;
    margin-left: 24px;
    flex-basis: 40%;
  
    &__heading{
      color: var(--gray300);
      text-transform: capitalize;
      font-size: 32px;
    }
    &__details{
      margin-top: 16px;
    }
    &__text{
      color: white;
      font-size: 20px;
    }
    &__info{
      margin-top: 48px;
      display: flex;
      flex-direction: column;
      gap: 32px;
    }
    &__icon{
      width: 30px;
      flex-shrink: 0;
    }

  }
  
  .location, .phone, .email{
    display: flex;
    align-items: center;
    gap: 24px;
  }
  .location-icon, .phone-icon{
    stroke: var(--gray500);
    fill: none;
  }
  .email-icon{
    fill: var(--gray500);
  }

  .social{
    margin: 32px auto 0;
    width: fit-content;

    &__heading{
      text-align: center;
      text-transform: capitalize;
      color: var(--gray300);
    }
    &__list{
      display: flex;
      gap: 24px;
      margin-top: 16px;
    }
    &__icon{
      width:32px
    }

  }

  @media screen and (max-width:1023px){
    .contact{
      max-width: 100%;
      margin-left: 0;
      flex-basis: auto;
      margin-top: 24px;
      padding: 32px 40px;
    }
  }

  @media screen and (max-width:767px){
      .contact{
        width: 100%;
        padding: 16px 24px;
        background-color: var(--blue);
        margin-bottom: 24px;
        margin-top: 0;

        &__heading{
          font-size: 24px;
        }
        &__details{
          display: none;
        }
        &__info{
          display: none;
        }
      }

  }
  
</style>