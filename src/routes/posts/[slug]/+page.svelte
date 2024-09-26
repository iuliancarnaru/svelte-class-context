<script lang="ts">
	import { page } from '$app/stores';
	import { getToastState } from '$lib/toast-state.svelte';

	import { onMount } from 'svelte';

	const toastState = getToastState();

	onMount(() => {
		toastState.add('Welcome to post!', 'We hope you enjoy this read!', 10000);
	});
</script>

<h1 class="text-lg font-semibold">Post {$page.params?.['slug']}</h1>
