<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';

	let linkActive = false;

	function clickLink(){
		linkActive = true
		
		return linkActive
		
	}
	var allLink = ['En savoir + sur moi', 'Portfolio', 'Les techs', 'Contacts', 'CV']
	var allLinkRedirect = ['#moi', '#portfolio', '#techs', '#contacts', '#CV']
	let i = 0;
</script>

<header class="head">
<ul class="head__list">
	{#each allLink as linkEl , index}
	<li class="head__el"><a href={allLinkRedirect[index]} class="head__link" class:active={'head__link--active'}  on:click={clickLink}> {linkEl}</a></li>
	
	{/each}
</ul>
</header>

<style>

.head{
	width: 55%;
	height: 80px;
	background-color: #B9B1A6;
	border-bottom: 3px solid #000;
	position: fixed;
	top: 0;
	right: 0;
}
.head__list{
	display: flex;
	flex-direction: row;
	width: 100%;
	height: 100%;
	justify-content: center;
	align-items: center;
	padding: 0 3vw;
}
.head__el{
	width: auto;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	
}

.head__link{
	font-family:var(--font-body);
	color: #000;
	padding: 12px 26px;
	transition: 0.3s;
	text-decoration: none;
	font-size: 18px;

}
.head__link:hover{
	transition: 0.2s;
	color: #fffcf8;
	font-family: var(--font-body-italic);
}
.head__link--active{
	color: blue;
	font-size: 800;
}
</style>
