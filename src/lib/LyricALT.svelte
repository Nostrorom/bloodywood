<script>
	import { slide, fade } from 'svelte/transition';
	export let show;
	export let lyric;

	let src;

	$: if (lyric.singer === 'Jayant') {
		src = '/band_pictures_Jayant.png';
	} else if (lyric.singer === 'Raoul') {
		src = '/band_pictures_Raoul.png';
	}
</script>

<div class="flex">
	<div class="w-14 relative">
		{#if lyric.singer !== ''}
			<img {src} class="w-full object-contain absolute top-0" alt={lyric.singer} />
		{/if}
	</div>

	<div class="pl-4 text-lg">
		{#if show.hindi && lyric.hindi}
			<p transition:slide class="text-yellow-400">{lyric.hindi}</p>
		{/if}
		{#if show.trans && lyric.trans}
			<p transition:slide class="text-yellow-400">{lyric.trans}</p>
		{/if}
		{#if show.eng || lyric.hindi === ''}
			<p>{lyric.eng}</p>
		{/if}
	</div>
</div>
