<script>
	import FullDetail from '../items/FullDetail.svelte';
	export let details;
</script>

<div>
	{#each details as { title, subtitle, link, dates, location, description, list }}
		<FullDetail {title} {subtitle} {link} {dates} {location} {description} {list} />
	{/each}
</div>
