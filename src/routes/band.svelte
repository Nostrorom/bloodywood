<script>
	import Icon from '$lib/Icon.svelte';
	import Video from '$lib/Video.svelte';
	let video = {
		id: 'HIvzfULOJ70',
		title: 'Raj Against The Machine',
		hindi: '',
		date: '2019',
		description:
			'Raj Against the Machine is a documentary that follows the journey of Bloodywood - a relatively unknown heavy metal band from the suburbs of India that shot to fame via a few viral music videos and went on to play sold out shows across Europe, UK, and the biggest heavy metal festival of the world - Wacken Open Air, on their very first tour itself. The band had never played a live show before this tour and the documentary unveils an emotional, hilarious and nerve-wracking story of how this seemingly impossible dream became a reality.'
	};
</script>

<div class="h-full w-full flex flex-col space-y-8">
	<Video {video} />

	<h6 class="text-3xl font-display text-gray-600">Section under construction</h6>
	<a href="https://www.facebook.com/displaywood.delhi/" target="_blank">
		<div class="flex">
			<div
				class="text-2xl flex items-center space-x-3 text-red-600 rounded-full hover:text-amber-400"
			>
				<div class="h-6">
					<Icon icon="out" />
				</div>
				<p>Link to Facebook page</p>
			</div>
		</div>
	</a>
	<a href="https://en.wikipedia.org/wiki/displaywood" target="_blank">
		<div class="flex">
			<div
				class="text-2xl flex items-center space-x-3 text-red-600 rounded-full hover:text-amber-400"
			>
				<div class="h-6">
					<Icon icon="out" />
				</div>
				<p>Link to Wikipedia</p>
			</div>
		</div>
	</a>
</div>
