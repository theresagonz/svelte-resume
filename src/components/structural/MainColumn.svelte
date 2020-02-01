<script>
  import Section from './Section.svelte';
	export let sections;
</script>

<div id="wide-column">
	{#each sections as { label, details, type }}
    <Section {label} {details} {type}></Section>
	{/each}
</div>

<style>
	#wide-column {
		width: 65%;
		margin: 0 var(--horizontal-space-between-columns);
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>
