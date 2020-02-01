<script>
	import SmallColumn from './SmallColumn.svelte';
	import LargeColumn from './LargeColumn.svelte';
	export const smallColumnSections = [
		{
			type: 'contact',
			label: 'Contact',
			details: [
				{
					subcategory: 'Say hello',
					contactDetails: [
						{
							isLink: true,
							type: 'email',
							text: 'test@gmail.com',
							icon: 'email',
						},
						{
							isLink: true,
							type: 'phone',
							text: '555-555-5555',
							icon: 'phone',
						},
						{
							text: 'Seattle, WA',
							icon: 'location',
						},
					],
				},
				{
					subcategory: 'Find me online',
					contactDetails: [
						{
							isLink: true,
							type: 'web',
							text: 'theresamorelli.com',
						},
						{
							isLink: true,
							type: 'web',
							text: 'github.com/theresamorelli',
							icon: 'github',
						},
						{
							isLink: true,
							type: 'web',
							text: 'linkedin.com/in/theresa-morelli',
							icon: 'linkedin',
						},
					],
				},
			],
		},
		{
			type: 'skills',
			label: 'Skills',
			details: [
				'JavaScript',
				'ES6',
				'React',
				'Redux',
				'MobX',
				'PostgreSQL',
				'MongoDB',
				'Express',
				'NodeJS',
				'Ruby on Rails',
				'jQuery',
				'WordPress',
				'HTML',
				'CSS',
				'Git',
				'Bootstrap',
				'Agile',
				'Jira',
			],
		},
		{
			type: 'short-details',
			label: 'Projects',
			details: [
				{
					title: 'Hello Pizza Truck',
					link: 'hellopizzatruck.com',
					subtitle: 'Website for selling food truck',
					description: 'Gatsby, React, Slick',
				},
				{
					title: 'Newsmash',
					link: 'newsmashed.herokuapp.com',
					subtitle: 'See the news differently',
					description: 'React, Redux, PostgreSQL, Ruby on Rails',
				},
			],
		},
	];
	export const largeColumnSections = [
		{
			type: 'full-details',
			label: 'Work Experience',
			details: [
				{
					title: 'Contract Full Stack Developer',
					subtitle: 'The Wally Shop',
					dates: `4/2019 — ongoing`,
					location: 'Remote',
					description: 'Reusable packaging grocery delivery service',
					list: [
						'Update and add new features to customer-facing e-commerce app using React, MobX, MaterialUI, Slick, and other external libraries.',
						'Implement MongoDB API endpoints and update schemas.',
						'Automate process to batch email PDFs after generating from graphics file.',
					],
				},
				{
					title: 'Front End Developer',
					subtitle: 'Sixcycle',
					dates: '4/2019 — 10/2019',
					location: 'Brooklyn, NY',
					description: 'Endurance coaching software used by Team in Training',
					list: [
						'Maintained ownership of the front end of a large web application powered by React, JavaScript, and custom libraries and state management.',
						'Designed and implemented new features, including message templates and community groups, from InVision prototypes.',
						'Improved and maintained code health and architecture for components including a message feed, training plan library, and calendar.',
						'Refactored to improve loading time and added error handling.',
					],
				},
				{
					title: 'Math Fellow, Americorps',
					subtitle: 'Denver Public Schools',
					dates: '8/2017 — 6/2018',
					location: 'Denver, CO',
					description: 'Middle school math intervention teacher',
					list: [
						'Created and taught lesson plans that included original worksheets, games, and activities to stimulate student engagement and meet requirements',
						'Developed a positive motivation system to encourage on-task behavior, teamwork, and delaying rewards.',
						'Launched and led HTML coding enrichment class with help from Galvanize students.',
					],
				},
			],
		},
		{
			type: 'full-details',
			label: 'Education',
			details: [
				{
					title: 'Online Software Engineering Program',
					subtitle: 'Flatiron School',
					dates: '2018 — 2019',
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
		flex-direction: var(--row-reverse);
		margin: 0 var(--horizontal-offset);
	}
</style>

<div class="main-body">
	<LargeColumn sections={largeColumnSections} />
	<SmallColumn sections={smallColumnSections} />
</div>
