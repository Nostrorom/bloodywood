<script>
	import { Be, Fr, Us, It, Gb, Es, De, Ch, Jp, Dk, Cz, Nl, At } from 'svelte-flagicon';
	export let flag;
</script>

<div
	class="rounded-full h-6 w-6 flex items-center justify-center overflow-hidden shadow-lg border border-gray-900"
>
	<div class="h-full relative">
		{#if flag === 'France'}
			<Fr />
		{:else if flag === 'Italy'}
			<It />
		{:else if flag === 'UK'}
			<Gb />
		{:else if flag === 'Germany'}
			<De />
		{:else if flag === 'Netherlands'}
			<Nl />
		{:else if flag === 'Czechia'}
			<Cz />
		{:else if flag === 'Austria'}
			<At />
		{:else if flag === 'Switzerland'}
			<Ch />
		{:else if flag === 'Spain'}
			<Es />
		{:else if flag === 'Denmark'}
			<Dk />
		{:else if flag === 'Belgium'}
			<Be />
		{:else if flag === 'USA'}
			<Us />
		{/if}
		<div
			class="absolute top-0 bg-gradient-to-tr from-gray-900 to bg-gray-200 bg-opacity-10 h-full w-full"
		/>
	</div>
</div>
