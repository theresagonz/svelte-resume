<script>
    import SimpleDetail from '../items/SimpleDetail.svelte';
    export let details;
  </script>
  
  <div>
    {#each details as { title, subtitle, link, description }}
      <SimpleDetail {title} {subtitle} {link} {description} />
    {/each}
  </div>
  