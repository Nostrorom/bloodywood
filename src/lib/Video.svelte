<script>
	export let video;
	let src = `https://www.youtube.com/embed/${video.id}`;
</script>

<div class="flex flex-col lg:flex-row p-6 lg:p-10">
	<iframe
		class="rounded-lg w-full h-72 px-4 lg:px-0 lg:w-2/5 shadow-xl"
		{src}
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
		allowfullscreen
	/>

	<div class="w-full lg:w-3/5 px-3 py-2 lg:py-0 lg:px-10 space-y-2">
		<div class="flex space-x-4">
			<h6 class="text-4xl font-bloody text-red-700">
				{video.title}
			</h6>
			<h6 class="text-4xl font-hindi text-red-700 opacity-60">
				{video.hindi}
			</h6>
		</div>
		<p class="lg:text-base text-gray-600 ">{video.date}</p>
		<p class="lg:text-base leading-relaxed">
			{video.description}
		</p>
	</div>
</div>
