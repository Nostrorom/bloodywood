<script>
	import Sidebar from '$lib/Sidebar.svelte';
	import { fade } from 'svelte/transition';
	import '../app.css';
	import logo from '/static/elephant_logo.jpg';

	let showBG = true;

	const cycleBG = () => {
		showBG = !showBG;

		setTimeout(() => cycleBG(), 5000);
	};

	cycleBG();
</script>

<svelte:head>
	<meta charset="UTF-8" />
	<meta
		name="description"
		content="Mixing influences, Bloodywood brings Indian vibes to high-energy metal. A sound like no other ! - Unofficial (for now?) fan site"
	/>
	<meta name="keywords" content="metal hindi" />
	<meta name="author" content="Nos Dev" />
	<script async src="https://www.googletagmanager.com/gtag/js?id=G-EPVCPJEX1H"></script>
	<script>
		window.dataLayer = window.dataLayer || [];
		function gtag() {
			dataLayer.push(arguments);
		}
		gtag('js', new Date());
		gtag('config', 'G-EPVCPJEX1H');
	</script></svelte:head
>
<main class="w-screen h-screen flex bg-black text-gray-400">
	<img src={logo} alt="logo Bloodywood" class="h-full w-full absolute opacity-10 object-cover" />
	{#if showBG}
		<img
			transition:fade={{ duration: 2500 }}
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

	<div
		class="h-full w-full overflow-y-auto px-16 lg:px-48 lg:py-8 absolute top-0 bg-black bg-opacity-30"
	>
		<slot />
	</div>
</main>
