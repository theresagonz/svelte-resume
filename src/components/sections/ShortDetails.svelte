<script>
    import ShortDetail from '../items/ShortDetail.svelte';
    export let details;
  </script>
  
  <div>
    {#each details as { title, subtitle, link, description }}
      <ShortDetail {title} {subtitle} {link} {description} />
    {/each}
  </div>
  