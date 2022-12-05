<script lang="ts">
  import { Accordion } from "stwui";

  let open = "";

  function handleClick(item: string) {
    if (open === item) {
      open = "";
    } else {
      open = item;
    }
  }
</script>

<Accordion>
  <Accordion.Item open={open === "item1"}>
    <Accordion.Item.Title slot="title" on:click={() => handleClick("item1")}>
      Item 1
    </Accordion.Item.Title>
    <Accordion.Item.Content slot="content">
      accordion_body
    </Accordion.Item.Content>
  </Accordion.Item>
  <Accordion.Item open={open === "item2"}>
    <Accordion.Item.Title slot="title" on:click={() => handleClick("item2")}>
      Item 2
    </Accordion.Item.Title>
    <Accordion.Item.Content slot="content">
      accordion_body
    </Accordion.Item.Content>
  </Accordion.Item>
  <Accordion.Item open={open === "item3"}>
    <Accordion.Item.Title slot="title" on:click={() => handleClick("item3")}>
      Item 3
    </Accordion.Item.Title>
    <Accordion.Item.Content slot="content">
      accordion_body
    </Accordion.Item.Content>
  </Accordion.Item>
</Accordion>
