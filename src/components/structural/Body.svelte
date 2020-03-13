<script>
	import SideColumn from './SideColumn.svelte';
	import MainColumn from './MainColumn.svelte';

	export const sideColumn = [
		{
			type: 'contact',
			label: 'Contact',
			details: [
				{
					subcategory: 'Say hi',
					contactDetails: [
						{
							isLink: true,
							type: 'email',
							text: 'theresa.l.morelli@gmail.com',
							icon: 'email',
						},
						{
							isLink: true,
							type: 'phone',
							text: '303-909-1445',
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
							url: 'bit.ly/2vJ0owX',
							text: 'theresamorelli.com',
						},
						{
							isLink: true,
							type: 'web',
							url: 'bit.ly/2Q0GoMV',
							text: 'github.com/theresamorelli',
							icon: 'github',
						},
						{
							isLink: true,
							type: 'web',
							url: 'bit.ly/2xjOx8M',
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
				'NodeJS',
				'MobX',
				'Redux',
				'Ruby on Rails',
				'MongoDB',
				'PostgreSQL',
				'jQuery',
				// 'Express',
				'HTML',
				'CSS',
				'Git',
				'Bootstrap',
				// 'Agile',
				// 'Jira',
			],
		},
		{
			type: 'simple-details',
			label: 'Projects',
			details: [
				{
					title: 'Hello Pizza Truck',
					url: 'http://bit.ly/2VXTVJ3',
					link: 'hellopizzatruck.com',
					description:
						'Static site for selling food truck. Built with Gatsby, React hooks, and Slick carousel.',
				},
				{
					title: 'Newsmash',
					url: 'http://bit.ly/2Ix2sKW',
					link: 'newsmashed.herokuapp.com',
					description:
						'Data visualization for the news. Integrated three external APIs with React/Redux app and PostgreSQL.',
				},
				{
					title: 'Svelte Resume',
					url: 'bit.ly/38E1FCO',
					link: 'bit.ly/svelte-resume',
					description:
						'Flexible and customizable PDF resume template built with Svelte.',
				},
			],
		},
	];
	export const mainColumn = [
		{
			type: 'full-details',
			label: 'Experience',
			details: [
				{
					title: 'Contract Full Stack Developer',
					subtitle: 'The Wally Shop',
					dates: `4/2019 — ongoing`,
					location: 'Remote',
					description: 'Reusable packaging grocery delivery service',
					list: [
						'Update and add new features to customer-facing e-commerce app using React with MobX and Bootstrap.',
						'Implement NodeJS API endpoints using MongoDB queries.',
						'Execute miscellaneous technical projects such as auto-generating unique PDFs from a graphics file.',

						// 'Implement product rating system to handle both numerical reviews and comments',
						// Use React.js to add prompts and visual cues for shoppers to update product and inventory information.
						// Contracted to develop tech stack focused on MongoDB, Express.js, React, Node.js.
					],
				},
				{
					title: 'Front End Developer',
					subtitle: 'Sixcycle',
					dates: '4/2019 — 10/2019',
					location: 'Brooklyn, NY',
					description: 'Endurance coaching software used by Team in Training',
					list: [
						'Maintained primary ownership of the front end of a React / JavaScript SaaS web app used by thousands of coaches and athletes daily.',
						'Implemented new features from InVision prototypes, including message templates and public community groups.',
						'Improved stability through bug fixes and refactoring to reduce tech debt.',
					],
				},
				{
					title: 'Math Fellow, Americorps',
					subtitle: 'Denver Public Schools',
					dates: '2017 — 2018',
					location: 'Denver, CO',
					description: 'Middle school math intervention program',
					list: [
						'Improved academic outcomes for a diverse student population by creating and teaching lesson plans that included original worksheets and activities.',
						'Developed a positive motivation system to encourage on-task behavior, teamwork, and delaying of rewards.',
						'Launched and led HTML coding enrichment class with Galvanize students.',
						// • Taught small-group 6th grade math intervention, writing and delivering original lessons.
						// • Managed behavior and relationships with a positive motivation system, restorative conversations, and supplemental tutoring.
						// • Facilitated an elective with Galvanize where students learned HTML and built websites (deployed and hosted by Galvanize).
					],
				},
				{
					title: 'Technical Writer',
					subtitle: 'KBC Advanced Technologies',
					dates: '2014 — 2015',
					location: 'Denver, CO',
					description: 'Oil refinery operations manuals',
					list: [
						'Produced high quality training manuals that included written content and Visio drawings, synthesizing information from various sources.',
					],
				},

				// Linkedin

					// 'Produced high quality training manuals for oil refinery operations to communicate how materials move through complex systems.',
					// 'Wrote clear, concise content with information compiled from client documents, photos, and detailed flow diagrams.'
					// 'Created Visio drawings of condensed stream and equipment information to assist with visual understanding.',

				// Honeybee Robotics, New York, NY
				// Operations Associate, 2012–2013
				// • Controlled project document streams and managed all incoming bills, serving as the main point of contact for vendors.
				// • Created a macro in Excel VBA to automate entry and processing of expense data.
				// • Updated and expanded company website and blog using Joomla!
			],
		},
		{
			type: 'full-details',
			label: 'Education',
			details: [
				{
					title: 'Software Engineering Program',
					subtitle: 'Flatiron School',
					dates: '2018 — 2019',
					location: 'Remote',
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
		flex-direction: var(--column-order);
		margin: 0 var(--horizontal-offset);
	}
</style>

<div class="main-body">
	<MainColumn sections={mainColumn} />
	<SideColumn sections={sideColumn} />
</div>
