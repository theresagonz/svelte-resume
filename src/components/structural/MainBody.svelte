<script>
	import SmallColumn from './SmallColumn.svelte';
  import LargeColumn from './LargeColumn.svelte';

  export const smallColumnSections = [
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
					subtitle: 'Website for selling food truck',
					description: 'Gatsby, React, Slick',
				},
				{
					title: 'Newsmash',
					link: 'http://newsmashed.herokuapp.com',
					subtitle: 'See the news differently',
					description: 'React, Redux, PostgreSQL, Ruby on Rails',
				},
			],
		},
	];
  export const largeColumnSections = [
		{
      type: 'primary',
      label: 'Experience',
			details: [
				{
					title: 'Contract Full Stack Developer',
					subtitle: 'The Wally Shop',
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
					title: 'Front End Developer',
					subtitle: 'Sixcycle',
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
					title: 'Math Fellow, Americorps',
					subtitle: 'Denver Public Schools',
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
			type: 'primary',
			label: 'Education',
			details: [
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

<style>
  div {
    display: flex;
    justify-content: space-between;
    /* flex-direction: row-reverse; */
    margin: 0 -25px;
  }
</style>

<div>
	<SmallColumn sections={smallColumnSections} />
  <LargeColumn sections={largeColumnSections} />
</div>
