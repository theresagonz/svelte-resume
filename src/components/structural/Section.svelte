<script>
	import Contact from '../sections/Contact.svelte';
	import Skills from '../sections/Skills.svelte';
	import Details from '../sections/Details.svelte';
	export let label;
	export let details;
	export let type;
</script>

<div class="section">
	<h2 class="section-label">{label}</h2>
	<hr class="section-underline" />
	{#if type === 'primary'}
		<Details {label} {details} />
	{:else if type === 'skills'}
		<Skills {label} {details} />
	{:else if type === 'contact'}
		<Contact {label} {details} />
	{/if}
</div>
