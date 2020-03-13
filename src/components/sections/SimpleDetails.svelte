<script>
    import SimpleDetail from '../items/SimpleDetail.svelte';
    export let details;
  </script>
  
  <div>
    {#each details as { title, subtitle, icon, url, link, description }}
      <SimpleDetail {title} {subtitle} {icon} {url} {link} {description} />
    {/each}
  </div>
  