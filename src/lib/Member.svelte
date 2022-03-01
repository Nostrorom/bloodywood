<script>
	import Icon from '$lib/Icon.svelte';
	import { slide } from 'svelte/transition';
	export let member;
</script>

<div class="flex flex-row py-4">
	<img src={member.image} alt={member.name} class="w-24 h-24 lg:w-32 lg:h-32" />

	<div transition:slide class="px-3 py-2 space-y-1">
		<div class="flex space-x-4">
			<h6 class="text-2xl font-display text-red-700">
				{member.name}
			</h6>
			<h6 class="text-4xl font-hindi text-yellow-500 opacity-75">
				{member.hindi}
			</h6>
		</div>
		<!-- <div>
			<Icon icon={member.icon} />
		</div> -->
		<p class="text-sm leading-relaxed">
			{member.instrument}
		</p>
	</div>
</div>
