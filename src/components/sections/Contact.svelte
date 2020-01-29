<script>
	export let details;
</script>

<style>
	#contact-section {
		line-height: 2em;
	}
</style>

<div id="contact-section">
	{#each details as { phone, email, city, linkedin, web, blog }}
		{#if email}
			<div class="contact-item">
				<i class="fa fa-envelope" />
				{email}
			</div>
		{/if}
		{#if phone}
			<div class="contact-item">
				<i class="fa fa-phone-alt" />
				{phone}
			</div>
		{/if}
		{#if city}
			<div class="contact-item">
				<i class="fa fa-map-marker-alt" />
				{city}
			</div>
		{/if}
		{#if web}
		<div class="contact-item">
			<i class="fa fa-link" />
			<a href="https://{web}">{web}</a>
		</div>
		{/if}
		{#if blog}
		<div class="contact-item">
			<i class="fa fa-pencil-alt" />
			<a href="https://{blog}">{blog}</a>
		</div>
		{/if}
		{#if linkedin}
			<div class="contact-item">
				<i class="fab fa-linkedin-in" />
				<a href="https://{linkedin}">{linkedin}</a>
			</div>
		{/if}
		{/each}
</div>
