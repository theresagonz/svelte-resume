<script>
	import Detail from '../items/Detail.svelte';
	export let details;
</script>

<div>
	{#each details as { title, subtitle, link, dates, location, description, list }}
		<Detail {title} {subtitle} {link} {dates} {location} {description} {list} />
	{/each}
</div>
