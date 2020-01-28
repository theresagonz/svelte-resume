<script>
	import Item from './item.svelte';
	export let label;
	export let items;
</script>

<div class="section">
	<h2 class="section-label">{label}</h2>
	<hr class="section-underline" />
	{#each items as { title, subtitle, link, dates, location, description, list }}
	  <Item {title} {subtitle} {link} {dates} {location} {description} {list}></Item>
	{/each}
</div>
