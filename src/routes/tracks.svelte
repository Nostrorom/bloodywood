<script>
	import Video from '$lib/Video.svelte';
	import videos from '$lib/videos.json';
</script>

<svelte:head>
	<title>Tracks - Bloodywood</title>
</svelte:head>

<div class="">
	{#each videos as video}
		<Video {video} />
	{/each}
</div>
