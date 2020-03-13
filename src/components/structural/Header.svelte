<script>
	export const name = 'Theresa Morelli';
	const summaryLines = [
		"Curious and adaptable software developer specializing in React and JavaScript with", "10 months of front end production experience. Building on a technical background, discovered programming through a VBA scripting project and never stopped exploring. Enthusiastic about supporting impactful tech with clean code and user-friendly design.",

		// Always thinking about the user experience
		// Always brainstorming app ideas

		// Recombining things in unexpected ways

		// meaningful and impactful
		// supporting the underdog

		// I enjoy data, design, and clean code.

		// Enjoy the act of creation as well as refactoring.

		// I like to build things I like to use.

		// Try to be thoughtful always.

		// stand out while being in my voice

		// "I'm a software engineer specializing in front end JavaScript and React with 10 months of production experience. With a background in technical work, I discovered coding through VBA scripting and never stopped exploring. I'm enthusiastic about using clean code and user-friendly design to support impactful tech."

		// 		I'm a curious and adaptable software engineer specializing in React and JavaScript with 10+ months of front end production experience. I strive to create user-friendly design for impactful tech with clean, thoughtful code. I've been programming since discovering scripting and block-based coding. I strive to be thoughtful in everything I do and believe in using technology to reimagine a better world.

		// nerd out over

		
		// I am a full stack software engineer with a specialization in front-end JavaScript. My experience includes building and maintaining applications with React.js, Node.js, Express, React Native, Redux, D3, MongoDB, TypeScript, HTML, and CSS, among many others. I view programming as a powerful medium for change, and I love diving into new technologies to build problem-solving tools.

		//with a desire to make the world better one line of code at a time. I've built with React, Javascript, and Ruby on Rails and enjoy thinking about data, design, and clean code.

		// I've contributed to technology-related projects in capacities ranging from research engineering to writing to teaching. I first discovered coding is cool while automating a number-crunching VBA script at an admin job and fully caught the bug when introducing HTML and Scratch to the middle school classroom.

		// The possibilities for carving structure out of chaos continually inspire me, and I'm passionate about solving real problems, fostering connection, and supporting the underdog. I'm looking for an opportunity to be pushed to new limits and to contribute to an exciting mission.

		// Github: @theresamorelli
		// Email: theresa.l.morelli@gmail.com
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
		width: 81%;
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
