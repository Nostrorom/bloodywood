<script>
	import Video from '$lib/Video.svelte';
	import videos from '$lib/videos.json';
</script>

<div class="px-24">
	{#each videos as video}
		<Video {video} />
	{/each}
</div>
