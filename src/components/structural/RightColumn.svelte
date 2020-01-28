<script>
	import Section from './Section.svelte';
	export const sections = [
		{
			type: 'contact',
			label: 'Contact',
			details: [
				{
					email: 'test@gmail.com',
					phone: '555-555-5555',
					city: 'Seattle, WA',
					linkedin: 'linkedin.com/in/theresa-morelli',
					web: 'theresamorelli.com',
					blog: 'medium.com/@theresamorelli',
				},
			],
		},
		{
			type: 'skills',
			label: 'Skills',
			details: [
				'JavaScript',
				'React',
				'Redux',
				'MobX',
				'jQuery',
				'PostgreSQL',
				'MongoDB',
				'Express',
				'Node',
				'Ruby on Rails',
				'HTML',
				'CSS5',
				'Git',
				'Agile',
				'Jira',
			],
		},
		{
			type: 'primary',
			label: 'Projects',
			details: [
				{
					title: 'Hello Pizza Truck',
					link: 'http://hellopizzatruck.com',
					subtitle: 'Marketing website for selling food truck',
					description: 'Gatsby, React, Slick',
				},
				{
					title: 'Newsmash',
					link: 'http://newsmashed.herokuapp.com',
					subtitle: 'A different way to visualize the news',
					description: 'React, Redux, PostgreSQL, Ruby on Rails',
				},
			],
		},
	];
</script>

<div id="right-column">
	{#each sections as { label, details, type }}
	<Section {label} {details} {type}></Section>
	{/each}
</div>

<style>
	#right-column {
		width: 34%;
	}
</style>
