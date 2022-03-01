<script>
	export let review;
	import Icon from '$lib/Icon.svelte';
</script>

<a href={review.href} target="_blank">
	<div class="space-y-1 group py-2">
		<div class="flex space-x-3 items-center">
			<h6 class="text-3xl font-display text-red-700">
				{review.author}
			</h6>
			<div class="flex items-center space-x-2">
				{#each Array(review.stars) as _}
					<div class="h-4 text-yellow-400">
						<Icon icon="star" />
					</div>
				{/each}
				{#each Array(review.of - review.stars) as _}
					<div class="h-4 text-gray-600">
						<Icon icon="star" />
					</div>
				{/each}
			</div>
		</div>
		<p class="lg:text-base text-gray-600 ">{review.date}</p>
		<p class="lg:text-base leading-relaxed">
			{review.excerpt}
		</p>
		<div class="flex">
			<div
				class="text-base flex items-center space-x-4 text-gray-500 rounded-full group-hover:text-yellow-400"
			>
				<div class="h-5">
					<Icon icon="out" />
				</div>
				<p>Read full review</p>
			</div>
		</div>
	</div>
</a>
