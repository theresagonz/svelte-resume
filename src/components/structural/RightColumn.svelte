<script>
  import Section from '../shared/Section.svelte';
	export const sections = [
		{
      type: 'contact',
      label: 'Contact',
      items: [{ phone: '555-555-5555'}]
    },
    {
      type: 'skills',
      label: 'Skills',
      items: ['bowhunting', 'air fishing'],
		},
		{
      type: 'primary',
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
          description: 'React, Redux, PostgreSQL, Ruby on Rails',
				},
			],
		},
	];
</script>

<div id="right-column">
	{#each sections as { label, items, type }}
	  <Section {label} {items} {type}></Section>
	{/each}
</div>

<style>
	#right-column {
		width: 35%;
	}
</style>
