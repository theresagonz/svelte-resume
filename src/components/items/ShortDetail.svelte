<script>
	import ContactItem from './ContactItem.svelte';
	export let title;
	export let subtitle;
	export let link;
	export let description;
	export let detail = {
		isLink: true,
		type: 'web',
		text: link,
	};
</script>

<style>
	.top {
		flex-direction: column;
		align-items: var(--center);
		margin-bottom: 3px;
  }
  
  .subtitle {
    margin-bottom: 4px;
  }

  a {
    font-size: 0.9em;
  }
</style>

<div class="detail-container">
	<div class="top">
		<h3 class="title">{title}</h3>
		<div class="subtitle">{subtitle}</div>
    {#if link}
      <ContactItem {detail} />
    {/if}
	</div>
	<div class="bottom">
		{#if description}
			<div class="description">{description}</div>
		{/if}
	</div>
</div>
