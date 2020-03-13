<script>
	import Section from './Section.svelte';
	export let sections;
</script>

<div id="side-column">
	{#each sections as { label, details, type }}
		<Section {label} {details} {type}></Section>
	{/each}
</div>

<style>
	#side-column {
		width: calc(100% - var(--main-column-width));
		margin: 0 var(--horizontal-space-between-columns);
		text-align: var(--more-centered);
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>