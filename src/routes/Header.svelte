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


	function openNav(e){
		//alert('open')
		let navActif = document.querySelector('.head__list');
		let btn = document.querySelector('.head__btn')
		//navActif.classList.toggle('head__list--actif')
		navActif.style.top = 0;
		if(navActif?.classList.contains('head__list--actif')){
			//navActif.classList.remove('head__list--actif')
			navActif.style.top = '100vh';
			btn.classList.remove('head__btn--actif')
			document.querySelector('main').style.display='flex'; 
		}else{
			navActif.style.top = '0';
			//navActif.classList.add('head__list--actif')
			document.querySelector('main').style.display='none'; 
			btn.classList.add('head__btn--actif')
		}
	}
</script>

<header class="head">
<ul class="head__list head__list--actif ">
	{#each allLink as linkEl , index}
	<li class="head__el"><a href={allLinkRedirect[index]} class="head__link" class:active={'head__link--active'}  on:click={clickLink}> {linkEl}</a></li>
	
	{/each}
</ul>
<button class="head__btn" on:click={openNav}>
	<span class="head__btnBarre"></span><span class="head__btnBarre"></span><span class="head__btnBarre"></span>
</button>
</header>

<style>

.head{
	width: 100%;
	height: 80px;
	background-color: #B9B1A6;
	border-bottom: 3px solid #000;
	position: fixed;
	bottom: 0;
	z-index: 4;
	right: calc( 0px);
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	padding: 12px 3vw;
	align-items: center;
}
.head__btn{
	width: 28px;
	height: 25px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	border: none;
	background-color: inherit;

}
.head__btn--actif{
	transform: translateX(50%);
}
.head__btnBarre{
	width: 100%;
	height: 4px;
	background-color: #000;
}
.head__list{
	opacity: 0;
	position: fixed;
	top: 100vh;
	width: 100vw;
	height: 100vh;
	z-index: -2;
	transition: 0.2s;
}
.head__list--actif{
	position: fixed;
	opacity: 1;
	top: 100vh;
	left: 0;
	transition: 0.6s;
	z-index: 0;
	background-color: #B9B1A6;
	font-size: 38px;
	height: calc(100vh - 80px);
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}
.head__el{
	width: auto;
	height: 50px;
	display: flex;
	justify-content: center;
	align-items: center;
	
}
.main__off{
	opacity: 0;
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

@media(min-width: 600px){
	.head{
	width: calc(64.5vw - 6px);
	height: 80px;
	position: fixed;
	top: 0;
	bottom: auto;
	right:0;
}
.head__btn{
	display: none;
}
.head__list{
	opacity: 1;
	position: relative;
	z-index: 4;
	top: 0;
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
}
</style>
