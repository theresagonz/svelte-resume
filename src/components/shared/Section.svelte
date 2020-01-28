<script>
	import Item from './item.svelte';
	export const label;
	export const items;
</script>

<div class="section">
	<h2 class="section-label">{label}</h2>
	<hr class="section-underline" />
	{#each items as { title, subtitle, dates, location, description, list }}
	  <Item {title} {subtitle} {dates} {location} {description} {list}></Item>
	{/each}
</div>
