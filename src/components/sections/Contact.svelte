<script>
	import ContactItem from '../items/ContactItem.svelte';
	export let details;
</script>

<style>
	#contact-section {
		margin-top: 14px; /* align baseline with adjacent component text */
	}

	.contact-subsection {
		margin-top: var(--vertical-space-between-subsections);
	}

	.contact-subhead {
		font-family: var(--accent-font);
		font-size: 1.1em;
		font-weight: 400;
		text-transform: uppercase;
	}

	.contact-items {
		margin: 3px 0 0 12px;
		line-height: 1.7em;
	}
</style>

<div id="contact-section">
	{#each details as { subcategory, contactDetails }}
		<div class="contact-subsection">
			{#if subcategory}
				<div class="contact-subhead">{subcategory}</div>
			{/if}
			<div class="contact-items">
				{#each contactDetails as detail}
					<ContactItem {detail} />
				{/each}
			</div>
		</div>
	{/each}
</div>
