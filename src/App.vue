<template>
<div class="global-container">
  <main class="invitation">

  </main>

    <section id="rsvp">
    <h2>LCV</h2>
    <p class="highlight">LCV bölümü mevcut haliyle burada yer alabiliyorsa süper olur. Eğer buraya koyma şansımız yoksa, o zaman da LCV için buraya bir buton / link koyup oradan LCV sayfasına yönlendirebiliriz.</p>
  </section>
  
  <section class="family-information">
    <h2 class="family-information__heading">We hope to see you at our wedding.</h2>

    <a class="mb-5" href="#rsvp">Tap here to RSVP.</a>

    <h3 class="family-information__subheading text-left">Families</h3>
    <p class="family-information__text">
      Arzu & Murat Büyükerk 
    </p>
    <p class="family-information__text mb-5 lg:mb-10">
      Hande Atalay - Ugur & İlknur Uralcan 
    </p>
    <div class="flex items-center lg:items-baseline mb-5 lg:mb-10">
      <h3 class="family-information__subheading">Date:</h3>
      <p class="family-information__text ml-2">
        September 17, 2022 - Saturday @ 19:00
      </p>
    </div>
    <div class="flex items-center lg:items-baseline mb-5 lg:mb-10">
      <h3 class="family-information__subheading">Location:</h3>
      <p class="family-information__text ml-2 ">
        Divan Kuruçesme Teras, Istanbul
      </p>
    </div>

    <p class="family-information__text mb-5 lg:mb-20">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, reiciendis recusandae ex aut, necessitatibus voluptatem mollitia voluptatum provident ullam voluptates.
    </p>

  </section>



  <section class="raffles">
    <img :src="require('./assets/images/raffles.png')" alt="raffles-logo" class="raffles__img">
    <h3 class="raffles__heading">
      We hope your stay in Istanbul is as comfortable as possible.
    </h3>
    <p class="raffles__text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur commodi similique illo officiis eaque, sequi itaque iure voluptate et facilis quam, excepturi, voluptatibus pariatur cupiditate beatae. Natus aut incidunt labore.
    </p>
  </section>


  <svg version="1.1" class="svg-filters" style="display:none;">
  <defs>
    <filter id="marker-shape">
      <feTurbulence type="fractalNoise" baseFrequency="0 0.15" numOctaves="1" result="warp" />
      <feDisplacementMap xChannelSelector="R" yChannelSelector="G" scale="30" in="SourceGraphic" in2="warp" />
    </filter>
  </defs>
</svg>
</div>

</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      test: "",
    }
  },

  methods: {

  },

}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-size: 62.5%;
  }

  html{
    scroll-behavior: smooth;
  }
  body{
    background-color: #efebe0;
  }

  .invitation{
    background-image: url("./assets/images/invite-org.jpg");
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    height: 90vh;
    width: 100vw;
  }

  @media screen and (min-width: 900px){
    .invitation{
      height: 90vh;
      background-position: center;
    }
  }

  .family-information{
    width: 100vw;
    display: flex;
    flex-direction: column;
    padding: 0 3rem;
    margin-bottom: 4rem;
    font-family: "Lato", sans-serif;
  }


  .family-information__heading{
    font-family: "Courgette", cursive;
    font-size: 2.2rem;
    font-weight: bold;
    text-align: center;
    text-transform: uppercase;
    margin: 2rem 0;
  }

  .family-information__subheading{
    font-size: 1.4rem;
    font-weight: bold;
  }


  .family-information__text{
    font-size: 1.4rem;
    line-height: 160%;
  }

  .family-information a{
    color: black;
    font-size: 1.4rem;
    text-decoration: underline;
    cursor: pointer;

  }

  @media screen and (min-width: 900px){
    .family-information{
      align-items: center;
      max-width: 50%;
      margin-left: auto;
      margin-right: auto;
    }

    .family-information a{
      font-size: 1.6rem;
      margin-bottom: 2rem;
    }

  .family-information__subheading{
    font-size: 1.6rem;
  }


    .family-information__text{
      font-size: 1.6rem;
      text-align: center;
    }
  }


  .raffles{
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 3rem 0;
    padding: 0 3rem;
    font-family: "Lato", sans-serif;
  }

  .raffles__img{
    width: 15rem;

  }

  .raffles__heading{
    font-family: "Courgette", cursive;
    font-size: 2.2rem;
    font-weight: bold;
    text-align: center;
    margin: 2rem 0;
  }

  .raffles__text{
    font-size: 1.4rem;
    line-height: 160%;

  }



  @media screen and (min-width: 900px){

    .raffles{
      max-width: 50%;
      margin-right: auto;
      margin-left: auto;
      margin-bottom: 10rem;
    }
  
    .raffles__text{
      font-size: 1.6rem;;
    }
  }


  #rsvp{
    border-top: 2px dashed gray;
    height: 30vh;
    width: 100vw;
    padding: 3rem;
    display: flex;
    align-items: center;
    flex-direction: column;
    font-family: "Lato", sans-serif;
    margin-bottom:3rem;

  }

  #rsvp h2{
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 2rem;
  }

  #rsvp p{
    font-size: 1.6rem;
    line-height: 160%;

  }

.highlight{
  position:relative;
}

.highlight:before{
  content:"";
  background-color: rgba(147, 199, 241, 0.678);
  width:100%;
  height:10em;
  position:absolute;
  z-index:-1;
  filter:url(#marker-shape);
  left:-0.25em;
  top: -1rem;
  padding:0 0.25em;
}



</style>
