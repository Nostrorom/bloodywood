<script>
	import Icon from '$lib/Icon.svelte';
	import Video from '$lib/Video.svelte';
	import Member from '$lib/Member.svelte';

	import members from '$lib/members.json';
	let video = {
		id: 'HIvzfULOJ70',
		title: 'Raj Against The Machine',
		hindi: '',
		date: '2019',
		description:
			'Raj Against the Machine is a documentary that follows the journey of Bloodywood - a relatively unknown heavy metal band from the suburbs of India that shot to fame via a few viral music videos and went on to play sold out shows across Europe, UK, and the biggest heavy metal festival of the world - Wacken Open Air, on their very first tour itself. The band had never played a live show before this tour and the documentary unveils an emotional, hilarious and nerve-wracking story of how this seemingly impossible dream became a reality.'
	};
</script>

<svelte:head>
	<title>Band - Bloodywood</title>
</svelte:head>

<div class="h-full w-full flex flex-col space-y-8">
	<Video {video} />

	<div class="grid grid-cols-2 pb-24">
		{#each members as member}
			<Member {member} />
		{/each}
	</div>
</div>
