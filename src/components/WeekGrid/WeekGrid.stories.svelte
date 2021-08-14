<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import WeekGrid from "./WeekGrid.svelte";
</script>

<Meta
  title="SvelteDates/WeekGrid"
  component={WeekGrid}
  argTypes={{
    days: { control: "array" },
  }}
/>

<Template let:args>
  <WeekGrid {...args} />
</Template>

<Story
  name="Default"
  args={{
    days: [1, 2, 3, 4, 5, 6, 7],
    width: 50,
  }}
/>
