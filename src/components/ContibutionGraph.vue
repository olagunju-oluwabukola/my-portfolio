<template>
    <div>
      <h2 class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10"> Contribution Graph</h2>
      <!-- Placeholder div where the chart will be injected -->
      <div id="github-contributions-calendar" class="w-full"></div>
    </div>
  </template>
  
  <script>
  import GitHubCalendar from 'github-calendar';
  
  export default {
    name: 'ContributionGraph',
    
    mounted() {
      // Initialize the GitHub contributions calendar for your GitHub username
      GitHubCalendar("#github-contributions-calendar", "olagunju-oluwabukola", {
        responsive: true, // Make it responsive
        tooltips: true,   // Show tooltips
      });
    },
    async fetchGitHubData() {
  try {
    const response = await fetch(`https://api.github.com/users/olagunju-oluwabukola/events`);
    const data = await response.json();
    this.contributions = this.processContributionData(data);
  } catch (error) {
    console.error('Failed to fetch contribution data:', error);
  }
},

processContributionData(events) {
  return events.filter(event => event.type === 'PushEvent');
}

  }
  </script>
  
  <style scoped>
  /* You can add any custom styles here if needed */
  #github-contributions-calendar {
    max-width: 100%;
    margin: 0 auto;
  }
  </style>
  