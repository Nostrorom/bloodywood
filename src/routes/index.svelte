<script context="module">
	export const prerender = true;
</script>

<script>
	import Icon from '$lib/Icon.svelte';
	import Review from '$lib/Review.svelte';
	import rakshak from '/static/rakshak_cover.jpg';
	import { fade, slide } from 'svelte/transition';
	import music from '$lib/json/music.json';
</script>

<svelte:head>
	<title>Bloodywood</title>
</svelte:head>
<div class="space-y-8">
	<div class="group pt-16 flex flex-col lg:flex-row justify-center items-center">
		<img src={rakshak} alt="Rakshak album cover" class="pb-8 lg:pb-0 lg:w-96" />
		<div transition:fade class="lg:px-10 space-y-4">
			<h6 class="text-4xl font-display font-bold text-yellow-500">
				Rakshak <em class="font-hindi opacity-70 text-red-600">रक्षक</em>
			</h6>
			<h6 class="text-3xl font-display font-bold text-gray-300">Our debut album is out now !</h6>
			<p class="text-base leading-relaxed">
				This body of work embodies who we are and what we believe in. While we did have interest
				from multiple labels, we decided to stay independent and portray our music in its truest,
				most honest form. We're very lucky to have support from all of you and hope to justify all
				you have done for us through this album. It was written with YOU in mind and all the stories
				you have shared with us through DMs, emails and, when we were lucky enough, in person. It is
				our deepest desire that the songs in this album resonate with you on a personal level, help
				you get through your day, and strengthen you for what lies beyond.
			</p>

			<p class="text-base text-gray-500 leading-relaxed">Rakshak क्षक means guardian in Hindi</p>
			<!-- <div class="flex">
					<div
						class="text-xl flex items-center space-x-3 text-red-600 rounded-full group-hover:text-red-600"
					>
						<div class="h-8">
							<Icon icon="out" />
						</div>
						<p transition:slide class="font-display text-3xl">Get it here</p>
					</div>
				</div> -->
		</div>
	</div>
	<div class="flex space-x-16">
		<div>
			<h6 class="font-display font-bold text-yellow-500 text-3xl pb-2">Download</h6>
			<div class="flex space-x-4">
				{#each music.download as item}
					<a href={item.link} targe="_blank">
						<div class="hover:text-red-600 space-y-1">
							<div class="h-6">
								<Icon icon={item.icon} />
							</div>

							<p class="text-xs">{item.name}</p>
						</div>
					</a>
				{/each}
			</div>
		</div>
		<div>
			<h6 class="font-display font-bold text-yellow-500 text-3xl pb-2">Stream</h6>
			<div class="flex space-x-4">
				{#each music.stream as item}
					<a href={item.link} targe="_blank">
						<div class="hover:text-red-600 space-y-1">
							<div class="h-6">
								<Icon icon={item.icon} />
							</div>

							<p class="text-xs">{item.name}</p>
						</div>
					</a>
				{/each}
			</div>
		</div>
		<div>
			<h6 class="font-display font-bold text-yellow-500 text-3xl pb-2">CD / Vinyl</h6>
			<div class="flex space-x-4">
				{#each music.physical as item}
					<a href={item.link} targe="_blank">
						<div class="hover:text-red-600 space-y-1">
							<div class="h-6">
								<Icon icon="vinyl" />
							</div>

							<p class="text-xs">{item.name}</p>
						</div>
					</a>
				{/each}
			</div>
		</div>
	</div>
	<div class="">
		<Review
			review={{
				author: 'Kerrang!',
				date: 'Feb. 2022',
				href: 'https://www.kerrang.com/album-review-bloodywood-rakshak-india-metal',
				stars: 4,
				of: 5,
				excerpt:
					'Bloodywood have a sound like no one else in the world right now. Rakshak is equal parts joyous, furious and incendiary and its creators look set to be the first Indian metal band to truly explode on a global scale.'
			}}
		/>
		<Review
			review={{
				author: 'Distorted Sound Magazine',
				date: 'Feb. 2022',
				href: 'https://distortedsoundmag.com/album-review-rakshak-bloodywood/',
				stars: 9,
				of: 10,
				excerpt:
					'It’s a throwback to the “everything goes” approach of the mid-90s when metal merged with whatever musical genre happened to be wandering past at the time, but is also a well-written, convincing statement of intent.'
			}}
		/>
	</div>
</div>
