<script>
  export let title;
  export let subtitle;
  export let link;
  export let description;
</script>

<style>
  .top {
    flex-direction: column;
    align-items: var(--center);
    margin-bottom: 3px;
  }
</style>

<div class="detail-container">
  <div class="top">
    <h3 class="title">{title}</h3>
    <div class="subtitle">{subtitle}</div>
    {#if link}
      <div class="link">
        <i class="fa fa-link"></i>
        <a href="{link}">{link}<a>
      </div>
    {/if}
  </div>
  <div class="bottom">
    {#if description}
    <div class="description">{description}</div>
    {/if}
  </div>
</div>