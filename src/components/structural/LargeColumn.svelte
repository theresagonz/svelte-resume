<script>
  import Section from './Section.svelte';
	export let sections;
</script>

<div id="big-column">
	{#each sections as { label, details, type }}
    <Section {label} {details} {type}></Section>
	{/each}
</div>

<style>
	#big-column {
		width: 65%;
		margin: 0 25px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>
