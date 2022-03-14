<script>
	import Lyric from './Lyric.svelte';
	export let song;
	let show = { trad: true, hindi: true, trans: true };

	$: if (show.trans === false && show.hindi === false) {
		console.log('noo');
		show.trans = true;
	}
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
	<div class="flex">
		<button
			on:click={() => {
				show.hindi = !show.hindi;
			}}>Show hindi</button
		>
		<button
			on:click={() => {
				show.trans = !show.trans;
			}}>Show hindi roman</button
		>
		<button
			on:click={() => {
				show.trad = !show.trad;
			}}>Show translation</button
		>
	</div>
	{#each song.lyrics as lyric}
		<Lyric {show} {lyric} />
	{/each}
</div>
