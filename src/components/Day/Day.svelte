<script>
  import cx from "classnames";

  export let day = "";
  export let width = "";
  export let firstInColumn = false;
  export let lastInColumn = false;
  export let firstInRow = false;
  export let lastInRow = false;
</script>

<div
  style={`width: ${width}px; height: ${width}px`}
  class:first-in-column={firstInColumn}
  class:last-in-column={lastInColumn}
  class:first-in-row={firstInRow}
  class:last-in-row={lastInRow}
>
  <span>
    {day}
  </span>
</div>

<style>
  div {
    border: 1px solid green;
    border-left: 0;
    border-top: 0;
  }

  .first-in-column {
    border-left: 1px solid green;
  }

  .first-in-row {
    border-top: 1px solid green;
  }

  div span {
    display: block;
    padding: 10px;
  }
</style>
