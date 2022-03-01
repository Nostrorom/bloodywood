<script>
	export let merch;
	import Icon from '$lib/Icon.svelte';
	import { fade } from 'svelte/transition';
</script>

<div class="flex py-6 lg:py-10">
	<div class="w-1/3">
		<img src={merch.image} alt={merch.title} class="w-full object-contain" />
	</div>

	<div transition:fade class="w-2/3 lg:w-3/5 px-3 py-2 lg:py-0 lg:px-10 space-y-2">
		<h6 class="text-3xl font-display text-red-700">
			{merch.title}
		</h6>
		<h6 class="text-lg text-yellow-500 opacity-75">
			{merch.US_price} $
		</h6>
		<p class="text-sm italic leading-relaxed">
			{@html merch.description}
		</p>
		<div class="flex space-x-4">
			<a
				href={merch.WW_link}
				target="_blank"
				class="flex items-center px-2 py-1 space-x-2 border border-yellow-500 hover:bg-yellow-500 rounded-xl hover:text-black"
			>
				<div class="h-5">
					<Icon icon="out" />
				</div>
				<p class=" ">Global store</p>
			</a>
			<a
				href={merch.US_link}
				target="_blank"
				class="flex items-center px-2 py-1 space-x-2 border border-yellow-500 hover:bg-yellow-500 rounded-xl hover:text-black"
			>
				<div class="h-5">
					<Icon icon="out" />
				</div>
				<p class=" ">US store</p>
			</a>
		</div>
	</div>
</div>
