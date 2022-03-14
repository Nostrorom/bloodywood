<script>
	import Lyric from './Lyric.svelte';
	export let song;
	let show = { eng: true, hindi: true, trans: true };
</script>

<div>
	<div class="flex space-x-4">
		<h6 class="text-4xl font-display font-bold text-red-700">
			{song.title.eng}
		</h6>
		<h6 class="text-4xl font-hindi text-yellow-500 opacity-60">
			{song.title.hindi}
		</h6>
	</div>
	{#each song.lyrics as lyric}
		<Lyric {show} {lyric} />
	{/each}
</div>
