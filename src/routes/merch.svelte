<script>
	import Merch from '$lib/Merch.svelte';
	import merchs from '$lib/merchs.json';
</script>

<svelte:head>
	<title>Merch - Bloodywood</title>
</svelte:head>

<div class="grid grid-cols-2 space-x-2 space-y-2">
	{#each merchs as merch}
		<Merch {merch} />
	{/each}
</div>
