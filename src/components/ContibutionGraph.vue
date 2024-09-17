
      
      
      <template>
        <h2 class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10"> Contribution Graph</h2>
  <div class="flex justify-center p-6">
    <div id="github-calendar"></div>
  </div>
</template>

<script>
import GitHubCalendar from 'github-calendar';
import 'github-calendar/dist/github-calendar-responsive.css'; 

export default {
  name: 'GitHubGraph',
  mounted() {
  
    GitHubCalendar("#github-calendar", "olagunju-oluwabukola", {
      responsive: true
    });
  }
}
</script>

<style scoped>

#github-calendar {
  max-width: 100%;
  background-color: #f7f8fa;
  border-radius: 0.5rem;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
}
</style>

  

