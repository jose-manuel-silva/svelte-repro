<script>
	import { resolve } from '$app/paths';
</script>

<a
	href={resolve('/[testID]', {
		testID: '1'
	})}>Test 1</a
>

<a
	href={resolve('/[testID]', {
		testID: '2'
	})}>Test 2</a
>
