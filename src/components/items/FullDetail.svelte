<script>
	import ContactItem from './ContactItem.svelte';
	export let title;
	export let subtitle;
	export let link;
	export let dates;
	export let location;
	export let description;
	export let list;
	let linkDetail = { text: link };
	let locationDetail = { text: location, icon: 'location' };
</script>

<style>
	.top {
		justify-content: space-between;
		align-items: baseline;
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
</style>

<div class="full-detail detail-container">
	<div class="top">
		<div class="top-left">
			<div class="title">{title}</div>
			<div class="subtitle">{subtitle}</div>
			{#if link}
				<ContactItem detail={linkDetail} />
			{/if}
		</div>
		<div class="top-right">
			{#if dates}
				<div class="dates">{dates}</div>
			{/if}
			{#if location}
				<ContactItem detail={locationDetail} />
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
