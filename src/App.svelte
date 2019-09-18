<script>
	export let name;
	import 'bulma/css/bulma.css'
	import { Input, Field, Button, Icon, Collapse, Modal } from 'svelma'
  
  let active = false
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}!</h1>

<Button class="block" on:click={() => active = !active}>Toggle</Button>
<Modal bind:active={active}>
  <Field label="Username" type="is-success" message="Username is available">
    <Input id="username" name="username" type="text" placeholder="Text input" />
</Field>
</Modal>