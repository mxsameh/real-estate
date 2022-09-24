<script>
import Header from "$lib/components/base/Header.svelte";
import Footer from "$lib/components/base/Footer.svelte";
import Help from "$lib/components/base/Help.svelte";
import Details from "$lib/components/project/Details.svelte";
import Amenities from "$lib/components/project/Amenities.svelte";
import Available from "$lib/components/project/Available.svelte";
import Location from "$lib/components/project/Location.svelte";
import SimilarProjects from "$lib/components/project/SimilarProjects.svelte";

  
  let project = {
    name:'Creek Town',
    details:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cursus proin auctor fames posuere lobortis neque, id tincidunt. Ut vitae eget risus aenean. Amet eu nibh enim, enim, nec convallis proin. Cras parturient nibh elit purus enim risus aenean aliquam sit. Sit vel suspendisse nunc, bibendum arcu ac adipiscing massa gravida. Proin sodales euismod viverra nullam.',
    amenities:['security', 'smart gate', 'golf cart', 'parking', 'sports area', 'bikes lane', 'kids area', 'swimming pool'],
    properties:{
      apartments:[
        {id:1, start: '3,300,000', type:'apartment', minArea: 60, maxArea: 100, beds: 2, baths: 1, img:'/p1.png'},
        {id:2, start: '2,700,000', type:'apartment', minArea: 120, maxArea: 170, beds: 3, baths: 2, img:'/p1.png'},
        {id:3, start: '2,700,000', type:'apartment', minArea: 120, maxArea: 170, beds: 3, baths: 2, img:'/p1.png'},
      ],
      villas:[
        {id:1, start: '5,700,000', type:'twin house', minArea:220, maxArea: 270, beds: 4, baths: 3, img:'/p1.png'},
        {id:2, start: '7,300,000', type:'stand alone', minArea: 310, maxArea: 400, beds: 5, baths: 5, img:'/p1.png'},
      ],
    },
    location:{
      details:['5 min to circle k', '10 mins to family park', '3 mins away from suez road'],
      url:'https://www.google.com/maps/place/Heart+Of+The+Capital/@30.0964679,31.3765554,17z/data=!3m1!4b1!4m5!3m4!1s0x1458174853f733f5:0xc57773e9e3082876!8m2!3d30.096462!4d31.3786884',
    },
    img:'/project.png',
    similarProjects : [
      {id:1, name:'mivida', price:'3,500,000', img:'/proj1.png', url:'/project/mivida'},
      {id:2, name:'hyde park', price:'2,300,000', img:'/proj2.png', url:'/project/hyde-park'},
    ],
  }

</script>

<Header color='white'/>

<main class="hero">
  <div class="hero__img" style={`background-image: url(${project.img})`}></div>
  <h1 class="hero__title">{project.name}</h1>
</main>

<div class="container">
  <div class="details">
    <Details details={project.details} />
    <Amenities amenities={project.amenities} />
  </div>
  <Location location={project.location} />
  <Available properties={project.properties} />
  <SimilarProjects projects={project.similarProjects} />
  <Help />
</div>

<Footer />

<style lang="scss">


  .hero{
    position: relative;

    &__img{
      width: 100%;
      aspect-ratio: 3 / 2;
      filter: brightness(.8);
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
    }
    &__title{
      position: absolute;
      bottom: 12px;
      left: 16px;
      color: white;
      font-size: 24px;
    }
  }

  @media screen and (min-width: 768px){
    .hero__title{
        font-size: 40px;
        bottom: 24px;
        left: 40px;
    }
  }

  @media screen and (min-width: 1024px){
    .hero__img{
      max-height: 100vh;
    }
    .hero__title{
      bottom: 40px;
      font-size: 64px;
    }
    .details{
      display: flex;
      gap: 5%
    }
  }
</style>