<script>
  import antoHome from "$lib/images/anto.webp";
  // logic goes here
</script>

<!-- markup (zero or more items) goes here -->
<div class="home__colGauche">
  <img
    src={antoHome}
    alt="Une photo de moi, antoni dumont. "
    class="home__img"
  />
  <div class="home__boxName">
    <h1 class="sect__title">Antoni Dumont</h1>
    <p class="sect__title sect__title--sub">AKA anto__dev</p>
  </div>
</div>

<style>
  /* styles go here */
  .home__colGauche {
    width: 100%;
    height: 60vh;
    position: relative;
    top: 0;
    left: 0;
    border-right: 3px solid #000;
    overflow: hidden;
  }
  .home__boxName {
    width: 90%;
    height: 100%;
    position: relative;
    z-index: 4;
    left: 18px;
    bottom: 55%;
    text-align: end;
    font-family: var(--font-title);
    
  }
  .sect__title {
    font-size: 20cqw;
    color: #fff3e1;
  }
  .sect__title--sub {
    font-size: 10cqw;
    color: #ffbe5c;
  }
  .home__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  @media (min-width: 600px) {
    .home__colGauche {
      width: 35vw;
      height: 100vh;
      position: fixed;
      overflow: hidden;

    }
    .sect__title {
      font-size: 5cqw;
    }
    .sect__title--sub {
      font-size: 2cqw;

    }
    .home__boxName {

    bottom: 35%;

  }
  }
</style>
