<script>
	import Song from '$lib/Song.svelte';
	import songs from '$lib/json/songs.json';
</script>

<svelte:head>
	<title>Lyrics - Bloodywood</title>
</svelte:head>

<div class="p-8">
	{#each songs as song}
		<Song {song} />
	{/each}
</div>
