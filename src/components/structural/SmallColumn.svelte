<script>
	import Section from './Section.svelte';
	export let sections;
</script>

<div id="small-column">
	{#each sections as { label, details, type }}
		<Section {label} {details} {type}></Section>
	{/each}
</div>

<style>
	#small-column {
		width: 35%;
		margin: 0 var(--horizontal-space-between-columns);
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>