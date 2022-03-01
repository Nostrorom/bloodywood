<script>
	import Concert from '$lib/Concert.svelte';
	import concerts from '$lib/Concerts.json';
</script>

<div class="">
	{#each concerts as concert}
		<Concert {concert} />
	{/each}
</div>
