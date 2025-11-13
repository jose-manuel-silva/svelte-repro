<script>
	import { resolve } from '$app/paths';
</script>

<a
	href={resolve('/[test]', {
		test: '1'
	})}>Test 1</a
>

<a
	href={resolve('/[test]', {
		test: '2'
	})}>Test 2</a
>
