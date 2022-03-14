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
			<img {src} class="w-full object-contain absolute top-2" alt={lyric.singer} />
		{/if}
	</div>
	{#if lyric.eng}
		<div class="pl-4 pb-2 text-lg">
			{#each lyric.eng as eng}
				<p class="text-gray-200">{eng}</p>
			{/each}
		</div>
	{:else}
		<div class="pl-4 text-lg flex justify-between items-center w-full">
			<div>
				{#if show.hindi && lyric.hindi}
					<p transition:slide class="text-red-300 pt-1 text-base">{lyric.hindi}</p>
				{/if}
				{#if show.trans && lyric.trans}
					<p transition:slide class="text-yellow-400">{lyric.trans}</p>
				{/if}
			</div>
			{#if show.trad && lyric.trad}
				<p transition:fade class="align-right">{lyric.trad}</p>
			{/if}
		</div>
	{/if}
</div>
