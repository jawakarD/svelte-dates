<script>
  import WeekGrid from "../WeekGrid/WeekGrid.svelte";

  export let noOfDays = 30;
  let weeks = [];

  for (let day = 1, week = 0; day <= noOfDays; day++) {
    const currentWeek = weeks[week] || [];
    weeks[week] = [...currentWeek, day];

    if (day % 7 === 0) {
      week += 1;
    }
  }
</script>

{#each weeks as week, i}
  <WeekGrid days={week} width={50} firstInRow={i === 0} />
{/each}
