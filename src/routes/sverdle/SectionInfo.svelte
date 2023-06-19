<script>
  import CardProject from "../CardProject.svelte";
  import TFEImg from "../../lib/images/cardImg1.jpg";
  import EdieImg from "../../lib/images/cardImg2.jpg";
  import discordImg from "../../lib/images/cardImg3.jpg";
  import archeoImg from "../../lib/images/archeoCard.jpg";
  import TechItem from "../TechItem.svelte";

  import reactLogo from  "../../lib/images/logo/reactjs.svg";
  import vueLogo from  "../../lib/images/logo/vue.svg";
  import svelteLogo from  "../../lib/images/logo/svelte.svg";
  import gitLogo from  "../../lib/images/logo/git.svg";
  import jsLogo from  "../../lib/images/logo/logo-javascript 1.svg";
  import reduxLogo from  "../../lib/images/logo/redux 1.svg";
  import figmaLogo from  "../../lib/images/logo/figma.svg";
  import fireLogo from  "../../lib/images/logo/firebase.svg";
  import sassLogo from  "../../lib/images/logo/sass.svg";
  import pyLogo from  "../../lib/images/logo/python.svg";
  import phpLogo from  "../../lib/images/logo/php.svg";
  import deisgnLogo from  "../../lib/images/logo/design.svg";
  import adobeLogo from  "../../lib/images/logo/adobe.svg";

  // logic goes here
  export let titleBox;
  export let txtBox;
  export let bgColor;
  export let marginFirst;
  export let idSect;
  export let cardPresence;
  export let techPresence;

  let allCardInfo = [
    {
      name: "ARCHEO ",
      sub: "24h - webbasement",
      img: archeoImg,
      link: 'http://antoni-dumont.be/projets/wb/'
    },
    {
      name: "Edie / landing",
      sub: "Défis  - Devchallenges.io",
      img: EdieImg,
      link:'https://www.edie.devchallenges.io.antoni-dumont.be/'
    },
    {
      name: "Discord clone",
      sub: "Perso  ",
      img: discordImg,
      link : 'https://discord-clone-926b5.web.app/'
    },
  ];

  let allTechInfo = [
    {
    name: 'React.js',
    img: reactLogo
  },
  {
    name: 'Vue',
    img: vueLogo
  },
  {
    name: 'Svelte.js',
    img: svelteLogo
  },{
    name: '.js',
    img: jsLogo
  },
  {
    name: 'SASS /SCSS',
    img: sassLogo
  },{
    name: 'Git',
    img: gitLogo
  },
  
  {
    name: 'Redux',
    img: reduxLogo
  },
  {
    name: 'Firebase',
    img: fireLogo
  },{
    name: 'Python',
    img: pyLogo
  },{
    name: 'Php',
    img: phpLogo
  },{
    name: 'Design / UX-UI / Atomic',
    img: deisgnLogo
  },{
    name: 'Figma',
    img: figmaLogo
  },{
    name: 'Adobe suite',
    img: adobeLogo
  },

  ]
</script>

<!-- markup (zero or more items) goes here -->
<section
  class="sect"
  id={idSect}
  style:background-color={bgColor}
  style:padding={marginFirst}
>
  <h2 class="sect__title sect__title--2">
    {titleBox}
  </h2>
  <p class="sect__txt">
    {txtBox}
  </p>
  <div class="sect__cardList">
    {#if cardPresence == true}
      {#each allCardInfo as cards}
        <CardProject
          titleCard={cards.name}
          Subtitle={cards.sub}
          imgCard={cards.img}
          linkProject={cards.link}
          cardWith={''}
        />
      {/each}
      <div class="sect__boxCard">
        <!-- {#if window.innerWidth >= 600}
        <CardProject titleCard={"TattooExplore / TFE "} Subtitle={'TFE - HEAJ'} imgCard={TFEImg} cardWith={ '40vw'} linkProject={'http://antoni-dumont.be/projets/tfe'} />

        {:else}
        <CardProject titleCard={"TattooExplore / TFE "} Subtitle={'TFE - HEAJ'} imgCard={TFEImg} cardWith={ '80vw'} linkProject={'http://antoni-dumont.be/projets/tfe'} />
        {/if} -->
        
      </div>
    {/if}
  </div>

  {#if techPresence === true}

  <div class="sect__techList">
    {#each allTechInfo as techs }
      <TechItem nameLinkImg={techs.name} linkTechImg={techs.img} />
    {/each}
  </div>
  {/if}
</section>

<style>
  /* styles go here */
  .sect {
    min-height: 50vh;
    width: auto;
    background-color: #fff3e1;
    padding: 20vh 3vw;
    /* padding: 0 3vw; */
  }

  .sect__cardList {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    overflow: hidden;
    flex-wrap: wrap;
    column-gap: 1vw;
    row-gap: 1vh;
    margin: 103px 0 0 calc(-3vw + 0px);
    width: calc(100% + 6vw);
    
  }
  .sect__boxCard{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    margin: 90px 0 0 0;
  }
  .sect__title {
    font-family: var(--font-title);
    font-size: 10cqi;
    
    margin: 0 0 51px 0;
  }

  .sect__txt {
    font-family: var(--font-body);
    font-size: 18px;
    line-height: 160%;
    
    padding: 0 3vw;
    
  }
  .sect__techList{
    width: 100%;display: flex;
    flex-direction: column;
    row-gap: 1vh;
    flex-wrap: wrap;
  }

  @media(min-width: 600px){
    .sect {
    width: 100%;
    padding: 20vh 3vw;
    /* padding: 0 3vw; */
  }
  .sect__txt {
    width: 70ch;
    
  }
  .sect__title {
    font-size: 4cqi;

  }
  .sect__cardList {

    column-gap: 1vw;
    margin: 103px 0 0 calc(-3vw + 0px);
    width: calc(100% + 6vw);
    
  }
  .sect__techList{
    height: 50vh;
    min-height: 300px;
    max-height: 400px;
    column-gap: 1vw;
    row-gap: 2vh;
  }
  }
</style>
