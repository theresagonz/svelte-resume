<script>
	const name = 'Theresa Morelli'
	import Header from './components/structural/Header.svelte';
	import Body from './components/structural/Body.svelte';
</script>

<main>
	<Header {name}/>
	<Body/>
</main>

<style>
@import url('https://fonts.googleapis.com/css?family=Lato:300,400,500|Open+Sans:300,400,500&display=swap');
@import '/styles/global.css';
	/* :global(main) {
		width: 8.5in;
		height: 11in;
		padding: 3em 4em;
		margin: 0 auto;
		font-family: 'Lato', sans-serif;
		--accent-color: rgb(12, 139, 218);
		--accent-font: 'Open Sans', sans-serif;
	}

	:global(.title) {
		font-size: 2em;
		color: red;	
	}

	:global(h1, h2, h3, h4, h5, h6) {
		/* font-family: 'Bitter'; */
	/*}
	*/

</style>
