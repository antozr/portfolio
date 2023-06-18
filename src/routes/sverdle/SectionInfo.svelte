<script>
	
	// logic goes here
    export let titleBox;
   export let txtBox;
   export let bgColor;
   export let marginFirst;
   export let idSect;
</script>

<!-- markup (zero or more items) goes here -->
<section class="sect" id={idSect} style:background-color={bgColor} style:padding={marginFirst}>
<h2 class="sect__title sect__title--2">
{titleBox}
</h2>
<p class="sect__txt">
    {txtBox}
</p>
</section>

<style>
	/* styles go here */
.sect{
    min-height: 90vh;
    /* width: 100%; */
    
    padding: 20vh 3vw 0 48.5%;
    /* padding: 0 3vw; */
    
}

.sect__title{
    font-family: var(--font-title);
    font-size: 4cqi;
    text-align: end;
    margin: 0 0 51px 0;
}

.sect__txt{
    font-family: var(--font-body);
    font-size: 18px;
    line-height: 160%;
}
</style>