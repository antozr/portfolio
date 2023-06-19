<script>
	import  antoHome  from '$lib/images/anto.webp';
	// logic goes here
   
</script>

<!-- markup (zero or more items) goes here -->
<div class="home__colGauche">
    <img src={antoHome} alt="Une photo de moi, antoni dumont. " class="home__img">
</div>

<style>
	/* styles go here */
    .home__colGauche{
        width: 35vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
        border-right: 3px solid #000;
    }
    .home__img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
</style>