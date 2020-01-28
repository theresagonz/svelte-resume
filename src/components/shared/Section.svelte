<script>
  import Item from './item.svelte';
  import ContactSection from '../shared/ContactSection.svelte';
  import SkillsSection from '../shared/SkillsSection.svelte';
	export let label;
  export let items;
  export let type;
</script>

<div class="section">
	<h2 class="section-label">{label}</h2>
  <hr class="section-underline" />
  {#if type === 'primary'}
    {#each items as { title, subtitle, link, dates, location, description, list }}
      <Item {title} {subtitle} {link} {dates} {location} {description} {list}></Item>
    {/each}
  {:else if type === 'skills'}
    <SkillsSection {label} {items}></SkillsSection>
  {:else if type === 'contact'}
    <ContactSection {label} {items}></ContactSection>
  {/if}
</div>
