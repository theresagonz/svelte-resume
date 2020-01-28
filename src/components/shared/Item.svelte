<script>
	export let title;
	export let subtitle;
	export let link;
	export let dates;
	export let location;
	export let description;
	export let list;
</script>

<div class="item-container">
	<div class="top">
		<div class="top-left">
			<h3 class="title">{title}</h3>
			<div class="subtitle">{subtitle}</div>
			{#if link}
				<div class="link"><i class="fa fa-link"></i><a href={link}>{link}<a></div>
			{/if}
		</div>
		<div class="top-right">
			{#if dates}
				<div class="dates">{dates}</div>
			{/if}
			{#if location}
				<div class="location"><i class="fa fa-map-marker-alt"></i>{location}</div>
			{/if}
		</div>
	</div>
	<div class="bottom">
		{#if description}
			<div class="description">{description}</div>
		{/if}
		{#if list}
			<ul class="list">
				{#each list as listItem}
				<li class="list-item">{listItem}</li>
				{/each}
			</ul>
		{/if}
	</div>
</div>

<style>
	.item-container {
		line-height: 1.4em;
		margin: 28px 0;
	}

	.item-container:first-of-type {
		margin-top: 0;
	}

	.top {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: baseline;
		margin-bottom: 3px;
	}

	.link {	
		font-size: 0.9em;
		color: var(--grey-mid)
	}

	.title {
		display: flex;
		justify-content: space-between;
		align-items: baseline;
		margin-bottom: 6px;
		font-family: var(--accent-font);
		color: var(--grey-dark);
	}

	.top-right,
	.top-left {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.top-right {
		align-items: flex-end;
		font-size: 0.9em;
		color: #000;
	}

	.location {
		padding-top: 3px;
	}

	.bottom {
		font-size: 0.95em;
	}
	
	.description {
		font-size: 1.05em;
	}

	.list {
		line-height: 1.3em;
	}

	.list-item {
		margin-bottom: 4px;
	}
</style>
