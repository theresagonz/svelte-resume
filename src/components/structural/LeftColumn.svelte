<script>
	import Section from '../shared/Section.svelte';
	export const sections = [
		{
			label: 'Work Experience',
			items: [
				{
					title: 'The Wally Shop',
					subtitle: 'Contract Full Stack Developer',
					dates: `4/2019 — ongoing`,
					location: 'Remote',
					description: 'Packaging-free grocery delivery service',
					list: [
						'Update customer-facing e-commerce app using React, MobX, JS, CSS',
						'Implement MongoDB API endpoints and update schemas',
						'One more thing',
					],
				},
				{
					title: 'Sixcycle',
					subtitle: 'Front End Developer',
					dates: '4/2019 — 10/2019',
					location: 'Brooklyn, NY',
					description:
						'Endurance training and coaching software used by Team in Training',
					list: [
						'Built new features like message templating and public groups',
						'Made improvements and fixed bugs for a variety of components, including message feed, training plan library, and calendar',
						'Refactored to improve loading time and added error handling',
					],
				},
				{
					title: 'Denver Public Schools',
					subtitle: 'Math Fellow, Americorps',
					dates: '8/2017 — 6/2018',
					location: 'Denver, CO',
					description: 'Middle school math intervention teacher',
					list: [
						'Created lesson plans that included original worksheets, games, and activities to make learning fun and meet requirements',
						'Developed a positive motivation system to encourage good behavior, teamwork, and delaying rewards',
						'Co-taught HTML coding elective, helping middle school students build hosted websites',
					],
				},
			],
		},
		{
			label: 'Education',
			items: [
				{
					title: 'Online Software Engineering Program',
					subtitle: 'Flatiron School',
					dates: '2018 — 2019',
					// location: 'online',
				},
				{
					title: 'B.S. Chemical Engineering',
					subtitle: 'Colorado School of Mines',
					dates: '2003 — 2007',
					location: 'Golden, CO',
				},
			],
		},
	];
</script>

<div id="left-column">
	{#each sections as { label, items }}
	  <Section {label} {items}></Section>
	{/each}
</div>

<style>
	#left-column {
		width: 65%;
		margin-right: 50px;
	}
</style>
