<script>
	export let detail;
	let { isLink, type, text, url, icon } = detail;
	let defaultIcon = 'fa fa-star';
	const fontAwesomeIconMap = {
		location: 'fa fa-map-marker-alt',
		email: 'fa fa-envelope',
		phone: 'fa fa-phone-alt',
		github: 'fab fa-github-alt',
		linkedin: 'fab fa-linkedin-in',
		blog: 'fa fa-pencil-alt',
	};
	let linkIcon = fontAwesomeIconMap[icon] || defaultIcon;
</script>

<style>
	.contact-item i {
		width: 20px;
		padding-right: 5px;
		font-size: 0.9rem;
		color: #000000bf;
		text-align: center;
	}
</style>

<div class="contact-item">
	<i class={linkIcon} />
	{#if isLink}
		{#if type === 'email'}
			<a href="mailto:{text}">{text}</a>
		{:else if type === 'phone'}
			<a href="tel:{text}">{text}</a>
		{:else if url}
			<a href="http://{url}">{text}</a>
		{:else}
			<a href="http://{text}">{text}</a>
		{/if}
	{:else}{text}{/if}
</div>
