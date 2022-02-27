<script>
	import Icon from '$lib/Icon.svelte';
	import Video from '$lib/Video.svelte';
	let video = {
		id: 'HIvzfULOJ70',
		title: 'RaJ agAinSt ThE MacHine',
		hindi: '',
		date: '2019',
		description:
			'"Dream no small dreams for they stir not the hearts of men." –Johann Wolfgang von Goethe. This is our story.'
	};
</script>

<div class="h-full w-full px-24 flex flex-col space-y-8 items-center justify-center">
	<Video {video} />

	<h6 class="text-3xl font-bloody text-gray-600">Section under construction</h6>
	<a href="https://www.facebook.com/bloodywood.delhi/" target="_blank">
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
	<a href="https://en.wikipedia.org/wiki/Bloodywood" target="_blank">
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
