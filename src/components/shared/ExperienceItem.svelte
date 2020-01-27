<!-- Use for job or education -->
<script>
  export let employer;
  export let title;
  export let dates;
  export let location;
  export let description;
  export let responsibilities;
</script>

<style></style>

<div class="experience-container">
  <h3>{employer}</h3>
  <h4>{title}</h4>
  <div><span>{dates}</span><span>{location}</span></div>
  {#if description}
    <div>{description}</div>
  {/if}
  <ul>
    {#if responsibilities}
      {#each responsibilities as resp}
      <li>{resp}</li>
      {/each}
    {/if}
  </ul>
</div>
