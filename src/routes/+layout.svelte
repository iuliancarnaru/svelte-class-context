<script lang="ts">
	import type { Snippet } from 'svelte';
	import Toaster from '../lib/components/toaster.svelte';
	import Nav from '../lib/components/nav.svelte';
	import '../app.css';
	import { setToastState } from '$lib/toast-state.svelte';

	let { children }: { children: Snippet } = $props();

	setToastState();
</script>

<Toaster />
<Nav />

<main class="p-4">
	{@render children()}
</main>
