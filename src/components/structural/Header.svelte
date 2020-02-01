<script>
	export const name = 'Theresa Morelli';
	const summaryLines = [
		'Curious and adaptable web developer with 10+ months of front end production experience. Especially skilled with React and currently learning more frameworks. Career history includes technical writing, education, and chemical engineering. Always thinking about the user experience. Always brainstorming app ideas.',

		// meaningful and impactful
		// supporting the underdog

		// I enjoy data, design, and clean code.

		// Enjoy the act of creation as well as refactoring.

		// I like to build things I like to use.

		// Try to be thoughtful always.
	];
</script>

<style>
	#header {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		text-align: center;
		margin-bottom: var(--vertical-space-between-sections);
	}

	#my-name {
		text-transform: uppercase;
		color: var(--accent-color);
		font-family: var(--accent-font);
		font-size: 3em;
		margin: 0;
	}

	.summary {
		width: 78%;
		margin-top: 5px;
		font-size: 1.05em;
		font-weight: 300;
		font-family: var(--accent-font);
		line-height: 1.5em;
		color: #000;
	}
</style>

<div id="header">
	<h1 id="my-name">{name}</h1>
	<div class="summary">
		{#each summaryLines as line, i}
			<div class="summary-line-{i}">
				{@html line}
			</div>
		{/each}
	</div>
</div>
