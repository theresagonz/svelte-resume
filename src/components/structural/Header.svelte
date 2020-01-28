<script>
	export let name;
	const summary =
		'Fashion axe farm-to-table vinyl vape. Bushwick artisan unicorn distillery. Helvetica knausgaard vice, selfies viral echo park kale chips 8-bit photo booth neutra 3 wolf moon gochujang venmo small batch tacos farm-to-table poutine tofu typewriter gentrify aesthetic.';
</script>

<style>
	#header {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-bottom: 35px;
		text-align: center;
	}

	#my-name {
		text-transform: uppercase;
    color: var(--accent-color);
		font-family: var(--accent-font);
		font-size: 3.5em;
		font-weight: 500;
		margin: 0;
	}

	.summary {
    width: 70%;
    margin-top: 10px;
    font-size: 1.2em;
    color: #000;
	}
</style>

<div id="header">
	<h1 id="my-name">{name}</h1>
	<div class="summary">{@html summary}</div>
</div>
