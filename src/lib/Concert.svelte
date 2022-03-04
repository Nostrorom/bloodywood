<script>
	import Icon from '$lib/Icon.svelte';
	import Flag from '$lib/Flag.svelte';
	import { slide } from 'svelte/transition';
	export let concert;

	const today = new Date();

	const date = new Date(concert.date);
	// const date = new Date("02/22/23")

	const diff = Math.round((date - today) / (1000 * 60 * 60 * 24));

	const month = date.toLocaleString('default', { month: 'long' });
	const day = date.getDate();
</script>

<a
	href={concert.buyTickets}
	target="_blank"
	class="flex flex-row group border rounded-md border-gray-500 border-opacity-0 hover:border-opacity-100 hover:shadow-lg hover:bg-opacity-40 hover:bg-black my-4"
>
	<div
		class="w-24 ring-1 rounded-md ring-gray-500 group-hover:ring-opacity-0 py-4 px-3 text-center"
	>
		<div class="">
			<div class="text-xl">
				{date.getDate()}
			</div>
			<div class="text-yellow-500">
				{month}
			</div>
			<div class="text-red-600 font-display text-xl">
				{date.getFullYear()}
			</div>
		</div>
		<div class="text-xs text-gray-500 pt-2">
			in {diff} days
		</div>
	</div>

	<div transition:slide class="px-4 py-4 space-y-1">
		<div class="flex space-x-3 items-center">
			<div>
				<Flag flag={concert.flag} />
			</div>
			<h6 class="text-2xl font-display font-bold text-red-700">
				{concert.country}
			</h6>
			<h6 class="text-2xl font-hindi text-yellow-500 opacity-70">
				{concert.city}
			</h6>
		</div>
		<div class="flex space-x-2 items-center pl-1.5">
			<div class="h-4">
				<Icon icon="marker" />
			</div>
			<p class="leading-relaxed">
				{concert.venue}
			</p>
		</div>
		<p class="text-sm text-gray-500 pl-1.5">
			{concert.price}
			{concert.currency}
		</p>
		<div class="pl-1 pt-2 flex items-center space-x-2 -full group-hover:text-yellow-500">
			<div class="h-5">
				<Icon icon="out" />
			</div>
			<p>Tickets</p>
		</div>
	</div>
</a>
