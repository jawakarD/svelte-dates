<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import MonthGrid from "./MonthGrid.svelte";
</script>

<Meta
  title="SvelteDates/MonthGrid"
  component={MonthGrid}
  argTypes={{
    noOfDays: { control: "text" },
  }}
/>

<Template let:args>
  <MonthGrid {...args} />
</Template>

<Story
  name="Default"
  args={{
    noOfDays: 31,
  }}
/>
