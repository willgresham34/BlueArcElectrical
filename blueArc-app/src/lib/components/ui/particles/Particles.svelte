<script lang="ts">
	import Particles, { particlesInit } from '@tsparticles/svelte';
	import { loadFull } from 'tsparticles'; // if you are going to use `loadFull`, install the "tsparticles" package too.

	export let count: number = 150;

	let particlesConfig = {
		particles: {
			color: {
				value: '#00000'
			},
			links: {
				enable: true,
				color: '#28609f',
				width: 1,
				distance: 100
			},
			move: {
				enable: true,
				speed: 1
			},
			number: {
				value: count
			}
		}
	};

	// Update config when count changes
	$: particlesConfig.particles.number.value = count;

	// @ts-ignore
	let onParticlesLoaded = (event) => {
		const particlesContainer = event.detail.particles;

		// you can use particlesContainer to call all the Container class
		// (from the core library) methods like play, pause, refresh, start, stop
	};

	void particlesInit(async (engine) => {
		// call this once per app
		// you can use main to customize the tsParticles instance adding presets or custom shapes
		// this loads the tsparticles package bundle, it's the easiest method for getting everything ready
		// starting from v2 you can add only the features you need reducing the bundle size
		await loadFull(engine);
		//await loadSlim(engine);
	});
</script>

<div class="particles-container">
	{#key count}
		<Particles id="tsparticles" options={particlesConfig} on:particlesLoaded={onParticlesLoaded} />
	{/key}
</div>

<style>
	.particles-container {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
	}
</style>
