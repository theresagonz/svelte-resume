<script>
	import ContactItem from './ContactItem.svelte';
	export let title;
	export let subtitle;
	export let url;
	export let link;
	export let icon;
	export let description;
	export let detail = {
		isLink: true,
		type: 'web',
		icon: icon,
		url: url,
		text: link,
	};
</script>

<style>
	.top {
		flex-direction: column;
		align-items: var(--more-centered);
		margin-bottom: 3px;
	}

	.simple-detail .top {
		margin-bottom: 7px;
	}

	.simple-detail:last-child {
		margin-bottom: 6px;
	}

  
  .subtitle {
    margin-bottom: 4px;
  }

  a {
    font-size: 0.9em;
  }
</style>

<div class="simple-detail detail-container">
	<div class="top">
		<div class="title">{title}</div>
		{#if subtitle}
			<div class="subtitle">{subtitle}</div>
		{/if}
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
