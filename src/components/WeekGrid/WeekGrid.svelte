<script>
  import Day from "../Day/Day.svelte";

  export let days = [];
  export let width = "";
  export let firstInRow = "";
</script>

<div>
  {#each days as day, i}
    <Day
      {width}
      {day}
      firstInColumn={i === 0}
      {firstInRow}
      last={i === days.length}
    />
  {/each}
</div>

<style>
  div {
    display: flex;
  }
</style>
