<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Day from "./Day.svelte";
</script>

<Meta
  title="SvelteDates/Day"
  component={Day}
  argTypes={{
    day: { control: "text" },
    width: { control: "text" },
  }}
/>

<Template let:args>
  <Day {...args} />
</Template>

<Story
  name="Default"
  args={{
    day: 20,
    width: 50,
  }}
/>

<Story
  name="First in column"
  args={{
    day: 20,
    width: 50,
    firstInColumn: true,
  }}
/>

<Story
  name="First in Row"
  args={{
    day: 20,
    width: 50,
    firstInRow: true,
  }}
/>

<Story
  name="First in Row and column"
  args={{
    day: 20,
    width: 50,
    firstInRow: true,
    firstInColumn: true,
  }}
/>
