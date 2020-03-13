<script>
	import Contact from '../sections/Contact.svelte';
	import Skills from '../sections/Skills.svelte';
	import FullDetails from '../sections/FullDetails.svelte';
	import SimpleDetails from '../sections/SimpleDetails.svelte';
	export let label;
	export let details;
	export let type;
</script>

<div class="section">
	<h2 class="section-label">{label}</h2>
	<hr class="section-underline" />
	{#if type === 'simple-details'}
		<SimpleDetails {label} {details} />
	{:else if type === 'full-details'}
		<FullDetails {label} {details} />
	{:else if type === 'skills'}
		<Skills {label} {details} />
	{:else if type === 'contact'}
		<Contact {label} {details} />
	{/if}
</div>
