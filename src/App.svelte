<script>
	export let name;
	name = 'Theresa Morelli'
	// $: console.log('name', name);
	import Header from './components/structural/Header.svelte';
	import Body from './components/structural/Body.svelte';
</script>

<main>
	<Header name={name}/>
	<Body/>
</main>

<style>
	main {
		width: 8.5in;
		height: 11in;
		padding: 3em 4em;
		margin: 0 auto;
	}

	:global(h1) {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
		margin: 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
