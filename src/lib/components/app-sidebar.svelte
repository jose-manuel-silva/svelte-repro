<script lang="ts" module>
	import BookOpenIcon from '@lucide/svelte/icons/book-open';
	import BotIcon from '@lucide/svelte/icons/bot';
	import Settings2Icon from '@lucide/svelte/icons/settings-2';
	import SquareTerminalIcon from '@lucide/svelte/icons/square-terminal';

	// This is sample data.
	const data = {
		navMain: [
			{
				title: 'Playground',
				url: '#',
				icon: SquareTerminalIcon,
				isActive: true,
				items: [
					{
						title: 'History',
						url: '#'
					},
					{
						title: 'Starred',
						url: '#'
					},
					{
						title: 'Settings',
						url: '#'
					}
				]
			},
			{
				title: 'Models',
				url: '#',
				icon: BotIcon,
				items: [
					{
						title: 'Genesis',
						url: '#'
					},
					{
						title: 'Explorer',
						url: '#'
					},
					{
						title: 'Quantum',
						url: '#'
					}
				]
			},
			{
				title: 'Documentation',
				url: '#',
				icon: BookOpenIcon,
				items: [
					{
						title: 'Introduction',
						url: '#'
					},
					{
						title: 'Get Started',
						url: '#'
					},
					{
						title: 'Tutorials',
						url: '#'
					},
					{
						title: 'Changelog',
						url: '#'
					}
				]
			},
			{
				title: 'Settings',
				url: '#',
				icon: Settings2Icon,
				items: [
					{
						title: 'General',
						url: '#'
					},
					{
						title: 'Team',
						url: '#'
					},
					{
						title: 'Billing',
						url: '#'
					},
					{
						title: 'Limits',
						url: '#'
					}
				]
			}
		]
	};
</script>

<script lang="ts">
	import NavMain from './nav-main.svelte';
	import * as Sidebar from '$lib/components/ui/sidebar/index.js';
	import type { ComponentProps } from 'svelte';

	let {
		ref = $bindable(null),
		collapsible = 'icon',
		...restProps
	}: ComponentProps<typeof Sidebar.Root> = $props();
</script>

<Sidebar.Root {collapsible} {...restProps}>
	<Sidebar.Content>
		<NavMain items={data.navMain} />
	</Sidebar.Content>
	<Sidebar.Rail />
</Sidebar.Root>
