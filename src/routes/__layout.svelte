<script>
	import Sidebar from '$lib/Sidebar.svelte';
	import { fade } from 'svelte/transition';
	import '../app.css';
	import logo from '/static/elephant_logo.jpg';

	let showBG = true;

	const cycleBG = () => {
		showBG = !showBG;

		setTimeout(() => cycleBG(), 6000);
	};

	cycleBG();
</script>

<svelte:head />
<main class="w-screen h-screen flex bg-black text-gray-400">
	<img src={logo} alt="logo Bloodywood" class="h-full w-full absolute opacity-10 object-cover" />
	{#if showBG}
		<img
			transition:fade={{ duration: 3000 }}
			src={logo}
			alt="logo Bloodywood"
			class="h-full w-full object-cover opacity-25"
		/>
	{/if}
	<div class="h-full fixed left-0 w-16 lg:w-48 z-10">
		<div class="h-full">
			<Sidebar />
		</div>
	</div>

	<div class="h-full w-full overflow-y-auto pl-16 lg:pl-48 absolute top-0 bg-black bg-opacity-40">
		<slot />
	</div>
</main>
