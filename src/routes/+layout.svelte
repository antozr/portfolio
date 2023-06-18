<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
		width: 100vw;
		
	}

	main {
		display: flex;
		flex-direction: row;
		box-sizing: border-box;
		
	}


	
</style>
