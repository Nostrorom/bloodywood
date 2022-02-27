<script>
	import { page } from '$app/stores';
	import Icon from '$lib/Icon.svelte';
	import sections from '$lib/sections.json';
	import logo from '/static/bloodywood_logo.png';
</script>

<header class="w-full h-full flex flex-col text-gray-700">
	<nav class="w-full h-4/5 my-auto">
		<ul class="h-full w-full flex flex-col justify-around">
			{#each sections as section}
				<li class="w-full font-display text-2xl lg:text-3xl">
					<a sveltekit:prefetch href={section.path}>
						<div
							class="h-32 group flex items-center hover:text-amber-400"
							class:text-red-600={$page.url.pathname === section.path}
						>
							<h5 class="w-4/5 leading-tight py-1 px-3 h-full flex items-center justifiy-center 0">
								{section.title}
							</h5>
							<div
								class="w-1/5 h-6 opacity-0 lg:opacity-100 justify-center group-hover:flex"
								class:hidden={$page.url.pathname !== section.path}
							>
								<Icon icon="meteor" />
							</div>
						</div>
					</a>
				</li>
			{/each}
		</ul>
	</nav>

	<div class="h-12 w-6 py-4 text-zinc-400 hover:text-amber-400">
		<a href="https://www.instagram.com/j.fidon/" target="_blank">
			<Icon icon="instagram" />
		</a>
	</div>
</header>
