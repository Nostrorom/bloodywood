<script context="module">
	export const prerender = true;
</script>

<script>
	import Icon from '$lib/Icon.svelte';
	import rakshak from '/static/rakshak_cover.jpg';
</script>

<svelte:head>
	<title>Bloodywood</title>
</svelte:head>

<section class="py-24 px-8 lg:px-24 flex flex-col lg:flex-row justify-center items-center">
	<img src={rakshak} alt="Rakshak album cover" class="pb-8 lg:pb-0 lg:w-96" />
	<div class="lg:px-10 space-y-4">
		<h6 class="text-4xl font-bloody text-amber-400">
			RAkShaK <em class="font-hindi opacity-70">रक्षक</em>
		</h6>
		<h6 class="text-3xl font-bloody text-gray-300">Our debut album is available for preorder !</h6>
		<p class="text-xl leading-relaxed">
			This body of work embodies who we are and what we believe in. While we did have interest from
			multiple labels, we decided to stay independent and portray our music in its truest, most
			honest form. We're very lucky to have support from all of you and hope to justify all you have
			done for us through this album. It was written with YOU in mind and all the stories you have
			shared with us through DMs, emails and, when we were lucky enough, in person. It is our
			deepest desire that the songs in this album resonate with you on a personal level, help you
			get through your day, and strengthen you for what lies beyond.
		</p>

		<p class="text-xl text-gray-500 leading-relaxed">Rakshak क्षक means guardian in Hindi</p>
	</div>
</section>
