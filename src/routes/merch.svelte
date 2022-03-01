<script>
	import Icon from '$lib/Icon.svelte';
</script>

<div class="h-full w-full pr-48 flex flex-col space-y-8 items-center justify-center">
	<h6 class="text-3xl font-bloody text-gray-600">Section under construction</h6>
	<a href="https://bloodywoodstore.com/" target="_blank">
		<div class="flex">
			<div
				class="text-2xl flex items-center space-x-3 text-red-600 rounded-full hover:text-yellow-500"
			>
				<div class="h-6">
					<Icon icon="out" />
				</div>
				<p>Link to global store</p>
			</div>
		</div>
	</a>
	<a href="https://bloodywoodstore.us/" target="_blank">
		<div class="flex">
			<div
				class="text-2xl flex items-center space-x-3 text-red-600 rounded-full hover:text-yellow-500"
			>
				<div class="h-6">
					<Icon icon="out" />
				</div>
				<p>Link to US store</p>
			</div>
		</div>
	</a>
</div>
