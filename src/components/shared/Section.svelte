<script>
	import ExperienceItem from './ExperienceItem.svelte';
	export let label;

	const jobs = [
		{
			employer: 'The Wally Shop',
			title: 'Contract Full Stack Developer',
			dates: `4/2019 — ongoing`,
			location: 'Remote',
			description: 'Packaging-free grocery delivery service',
			responsibilities: [
				'Update customer-facing e-commerce app using React, MobX, JS, CSS',
				'Implement MongoDB API endpoints and update schemas',
				'One more thing',
			],
		},
		{
			employer: 'Sixcycle',
			title: 'Front End Developer',
			dates: '4/2019 — 10/2019',
			location: 'Brooklyn, NY',
			description:
				'Endurance training and coaching software used by Team in Training',
			responsibilities: [
				'Built new features like message templating and public groups',
				'Made improvements and fixed bugs for a variety of components, including message feed, training plan library, and calendar',
				'Refactored to improve loading time and added error handling',
			],
		},
		{
			employer: 'Denver Public Schools',
			title: 'Math Fellow, Americorps',
			dates: '8/2017 — 6/2018',
			location: 'Denver, CO',
			description: 'Middle school math intervention teacher',
			responsibilities: [
				'Created lesson plans that included original worksheets, games, and activities to make learning fun and meet requirements',
				'Developed a positive motivation system to encourage good behavior, teamwork, and delaying rewards',
				'Taught HTML coding elective, helping middle school students build hosted websites',
			],
		},
	];
</script>

<style></style>

<div class="section">
	<h2 class="section-label">{label}</h2>
	<hr class="section-underline" />
	{#each jobs as { employer, title, dates, location, description,
	responsibilities }}
	<ExperienceItem
		{employer}
		{title}
		{dates}
		{location}
		{description}
		{responsibilities}
	></ExperienceItem>
	{/each}
</div>
