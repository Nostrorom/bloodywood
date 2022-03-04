<script>
	import Concert from '$lib/Concert.svelte';
	import concertsJSON from '$lib/json/concerts.json';

	$: console.log(concertsJSON.length);

	const concerts = [];

	Object.values(concertsJSON).forEach((concert) => {
		concert.date = new Date(concert.date);
		concerts.push(concert);
	});

	concerts.sort((a, b) => {
		return a.date - b.date;
	});
</script>

<svelte:head>
	<title>Tour - Bloodywood</title>
</svelte:head>

<div class="grid lg:grid-cols-2">
	{#each concerts as concert}
		<Concert {concert} />
	{/each}
</div>
