<script>
	import * as Dialog from '$lib/components/ui/dialog/index.js';
	let open = false;
</script>

<Dialog.Root bind:open>
	<Dialog.Trigger>Open</Dialog.Trigger>
	<Dialog.Content>
		<Dialog.Header>
			<Dialog.Title>You shouldn't be seeing this yet!</Dialog.Title>
		</Dialog.Header>
	</Dialog.Content>
</Dialog.Root>
