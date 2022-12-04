<script lang="ts">
  import { Alert, Button } from "stwui";

  const clear = "svg-path";
  const close = "svg-path";
</script>

<Alert>
  <Alert.Title slot="title">Title</Alert.Title>
</Alert>

<Alert type="warn">
  <Alert.Title slot="title">Title</Alert.Title>
</Alert>

<Alert type="error">
  <Alert.Leading slot="leading" data={clear} />
  <Alert.Title slot="title">Title</Alert.Title>
  <Alert.Description slot="description">I am a description</Alert.Description>
  <Alert.Extra slot="extra">
    <Button
      ariaLabel="close"
      shape="circle"
      on:click={() => console.log("I clicked extra")}
    >
      <Button.Icon slot="icon" data={close} />
    </Button>
  </Alert.Extra>
</Alert>
