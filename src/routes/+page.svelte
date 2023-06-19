<script>
  import Counter from "./Counter.svelte";
  import welcome from "$lib/images/svelte-welcome.webp";
  import welcome_fallback from "$lib/images/svelte-welcome.png";
  import antoHome from "$lib/images/anto.webp";
  import Photo from "./Photo.svelte";
  import SectionInfo from "./sverdle/SectionInfo.svelte";

  let allTxtSect = [
    "Bien le bonjour 👋, je suis un jeune diplômé en web design / développement front. \n \n Je me passionne pour le développement depuis quelques années, et la résolution des problèmes que je peux rencontrer dans le code et comment je peux les résoudre. Je jongle avec le .js et les différents frameworks pour pouvoir créer des projets avec un design et une expérience utilisateurs aux mieux.",
    "Voici quelques projets que j’ai réalisés dans un cadre scolaire ou non, et avec des objectifs différents.",
    "",
  ];
</script>

<svelte:head>
  <title>Portfolio / Antoni Dumont</title>
  <meta
    name="description"
    content="Vous vous trouvez sur le portfolio de Dumont Antoni, un jeune diplômé de la HEAJ en section Design Web Transmédia. Amusez-vous bien. "
  />
</svelte:head>

<section class="home">
  <Photo />
  <div class="home__list">
    <SectionInfo
      titleBox={"Moi en quelque mots : "}
      txtBox={allTxtSect[0]}
      bgColor={""}
      marginFirst={"40vh 3vw 0 "}
      idSect={"moi"}
    />
    <SectionInfo
      titleBox={"Mon portfolio :"}
      txtBox={allTxtSect[1]}
      bgColor={"#FFBE5C"}
      marginFirst={""}
      idSect={"portfolio"}
      cardPresence={true}
    />
    <SectionInfo
      titleBox={"Les techs :"}
      txtBox={allTxtSect[1]}
      bgColor={""}
      marginFirst={""}
      idSect={"techs"}
      cardPresence={""}
    />
    <SectionInfo
      titleBox={"Me contacter :"}
      txtBox={allTxtSect[1]}
      bgColor={"#FFBE5C"}
      marginFirst={""}
      idSect={"portfolio"}
      cardPresence={""}
    />
  </div>
</section>

<style>
  .home {
    display: flex;
    flex-direction: column;
    width: 100%;
    min-height: 100vh;
    overflow-x: hidden;
  }
  .home__list {
    display: flex;
    flex-direction: column;
    width: 100vw;
    position: relative;
    margin: 0 0 0 0vw;
  }

  @media(min-width: 600px){
    .home {
    display: flex;
    flex-direction: row;
    width: 100%;
    min-height: 100vh;
    overflow-x: hidden;
  }
  .home__list {
    width: calc(65vw - 3px);
    margin: 0 0 0 35vw;
  }
  }
</style>
