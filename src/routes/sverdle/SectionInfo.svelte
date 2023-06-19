<script>
  import CardProject from "../CardProject.svelte";
  import TFEImg from "../../lib/images/cardImg1.jpg";
  import EdieImg from "../../lib/images/cardImg2.jpg";
  import discordImg from "../../lib/images/cardImg3.jpg";

  // logic goes here
  export let titleBox;
  export let txtBox;
  export let bgColor;
  export let marginFirst;
  export let idSect;
  export let cardPresence;

  let allCardInfo = [
    {
      name: "TattooExplore / TFE",
      sub: "TFE - HEAJ",
      img: TFEImg,
    },
    {
      name: "Edie / landing",
      sub: "Défis  - Devchallenges.io",
      img: EdieImg,
    },
    {
      name: "Discord clone",
      sub: "Perso  ",
      img: discordImg,
    },
  ];
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
        />
      {/each}
    {/if}
  </div>
</section>

<style>
  /* styles go here */
  .sect {
    min-height: 50vh;
    width: 50vw;
    background-color: #fff3e1;
    padding: 20vh 3vw;
    /* padding: 0 3vw; */
  }

  .sect__cardList {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    column-gap: 1vw;
    margin: 103px 0 0 calc(-3vw + 0px);
    width: calc(100% + 6vw);
  }
  .sect__title {
    font-family: var(--font-title);
    font-size: 4cqi;
    text-align: end;
    margin: 0 0 51px 0;
  }

  .sect__txt {
    font-family: var(--font-body);
    font-size: 18px;
    line-height: 160%;
  }
</style>
