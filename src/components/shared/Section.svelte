<script>
  import ExperienceItem from './ExperienceItem.svelte';

  export let label;

  const jobs = [
    {
      employer: 'The Wally Shop',
      title: 'Contract Full Stack Developer',
      dates: '04/2019 - ongoing',
      location: 'Remote',
      description: 'Packaging-free grocery delivery service',
      responsibilities: [
        'Update customer-facing e-commerce app using React, MobX, JS, CSS',
        'Implement MongoDB API endpoints and update schemas',
        'One more thing',
      ],
    },
    {
      employer: 'Sixcycle',
      title: 'Front End Developer',
      dates: '04/2019 - 10/2019',
      location: 'Brooklyn, NY',
      description: 'Endurance training and coaching software used by Team in Training',
      responsibilities: [
        'Built new features like message templating and public groups',
        'Made improvements and fixed bugs for a variety of components, including message feed, training plan library, and calendar',
        'Refactored to improve loading time and added error handling',
      ],
    },
    { employer: 'Denver Public Schools', title: 'Math Fellow, Americorps', dates: '08/2017 - 06/2018', location: 'Brooklyn, NY' },
  ];
  
</script>

<style>
  h2 {
    text-transform: capitalize;
  }
</style>

<div class="section">
  <h2>{label}</h2>
  {#each jobs as { employer, title, dates, location, description, responsibilities }}
    <ExperienceItem {employer} {title} {dates} {location} {description} {responsibilities} />
    <hr/>
  {/each}
</div>