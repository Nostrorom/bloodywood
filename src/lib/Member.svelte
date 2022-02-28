<script>
	import Icon from '$lib/Icon.svelte';
	import { slide } from 'svelte/transition';
	export let member;
</script>

<div class="flex flex-col lg:flex-row">
	<img src={member.image} alt={member.name} class="pb-8 lg:pb-0 lg:w-96" />

	<div transition:slide class="w-full lg:w-3/5 px-3 py-2 lg:py-0 lg:px-10 space-y-2">
		<div class="flex space-x-4">
			<h6 class="text-4xl font-display text-red-700">
				{member.name}
			</h6>
			<h6 class="text-4xl font-hindi text-amber-400 opacity-75">
				{member.hindi}
			</h6>
		</div>
		<div>
			<Icon icon={member.icon} />
		</div>
		<p class="lg:text-base leading-relaxed">
			{member.instrument}
		</p>
	</div>
</div>
