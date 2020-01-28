<script>
  import Section from '../shared/Section.svelte';
	export const sections = [
		{
      label: 'Contact',
      items: [],
    },
    {
      label: 'Skills',
      items: [],
		},
		{
			label: 'Projects',
			items: [
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
          description: 'React, Redux, PostgreSQL, Ruby on Rails, external APIs',
				},
			],
		},
	];
</script>

<div id="right-column">
	{#each sections as { label, items }}
	  <Section {label} {items}></Section>
	{/each}
</div>

<style>
	#right-column {
		width: 35%;
	}
</style>
