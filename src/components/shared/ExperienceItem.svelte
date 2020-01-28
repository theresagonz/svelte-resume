<script>
	export let employer;
	export let title;
	export let dates;
	export let location;
	export let description;
	export let responsibilities;
</script>

<style>
	.job-container {
		line-height: 1.4em;
		margin: 28px 0;
	}

	.job-container:first-of-type {
		margin-top: 0;
	}

	.job-top {
		margin-bottom: 0.5em;
	}

	.employer-name {
		font-size: 1.1em;
		font-weight: 300;
	}

	.job-head {
		display: flex;
		justify-content: space-between;
		align-items: baseline;
		margin-bottom: 6px;
		font-family: var(--accent-font);
		color: var(--grey-dark);
	}

	.job-head-right,
	.job-head-left {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.job-head-right {
		align-items: flex-end;
		font-size: 0.9em;
		color: #000;
	}

	.location {
		padding-top: 3px;
	}

	.job-summary {
		font-size: 1em;
		font-weight: 400;
	}

	.job-bottom {
		font-size: 0.95em;
	}

	.job-duties {
		line-height: 1.3em;
	}

	.job-duty {
		margin-bottom: 4px;
	}
</style>

<div class="job-container">
	<div class="job-head">
		<div class="job-head-left">
			<h3 class="main-head">{title}</h3>
			<div class="subhead">{employer}</div>
		</div>
		<div class="job-head-right">
			<div class="dates">{dates}</div>
			<div class="location"><i class="fa fa-map-marker-alt"></i>{location}</div>
		</div>
	</div>
	<div class="job-bottom">
		{#if description}
		<div class="job-summary">{description}</div>
		{/if}
		<ul class="job-duties">
			{#if responsibilities} {#each responsibilities as resp}
			<li class="job-duty">{resp}</li>
			{/each} {/if}
		</ul>
	</div>
</div>
