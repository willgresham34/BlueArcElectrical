<script lang="ts">
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import Particles from '$lib/components/ui/particles/Particles.svelte';
	//import Autoplay from 'embla-carousel-autoplay';
	//import { carouselPhotos } from '$lib/carouselPhotos';

	//const plugin = Autoplay({ delay: 5000, stopOnInteraction: true });
</script>

<div class="w-full">
	<div class="background-container">
		<div class="flex w-full items-center justify-center" id="homeBanner">
			<div class="bannerText flex flex-col items-center">
				<h1 class=" rounded-lg p-2 text-white">Your New Age Electrical Specialist</h1>
				<span class="bannerSubText"></span>
			</div>
		</div>
	</div>

	<div class="bg-primary w-full">
		<div class="text-card-foreground m-8 flex h-full flex-col items-center gap-4 pb-8 pt-4">
			<h2 class="">Welcome Home!</h2>
			<h3 class="">
				At Blue Arc Electrical, we provide top-tier residential and commercial electrical services
				with a focus on safety, efficiency, and reliability.
			</h3>
			<h3>
				Serving Metro Atlanta, our licensed and insured electricians specialize in wiring, panel
				upgrades, lighting installations, EV charger setups, and more with quality craftsmanship
				never seen before!
			</h3>
			<div class="mt-2">
				<a
					href="/contact"
					class="bg-secondary hover:bg-secondary-foreground rounded-lg px-6 py-3 text-lg text-white"
					>Get Free Estimate!</a
				>
			</div>
		</div>
	</div>
	<!-- <div class="carousel mb-4">
		<Carousel.Root plugins={[plugin]}>
			<Carousel.Content>
				{#each carouselPhotos as photo}
					<Carousel.Item class=" basis-1/2 sm:basis-1/3 lg:basis-1/4 xl:basis-1/5"
						><img src={`/builds/${photo}`} alt="build1" /></Carousel.Item
					>
				{/each}
			</Carousel.Content>
		</Carousel.Root>
	</div> -->
	<div class="my-4 grid w-full grid-cols-1 sm:grid-cols-2">
		<div class="grid-item mb-8 flex items-center justify-center sm:mb-0">
			<section class=" h-auto rounded-lg">
				<div class="mx-auto px-4 text-white">
					<h2 class=" bg-primary rounded-lg px-4">Services We Handle</h2>
					<div class="text-center sm:text-start">
						<ul class="  my-2 grid grid-cols-1 gap-2 rounded-lg py-2 sm:grid-cols-1">
							<li class="bannerSubText">Fixture Installation</li>
							<li class="bannerSubText">Panel Upgrade</li>
							<li class="bannerSubText">Rewiring Projects</li>
							<li class="bannerSubText">EV Charger Setups</li>
						</ul>
					</div>
				</div>
			</section>
		</div>
		<div class="grid-item flex w-full items-center justify-center">
			<div class="w-1/3 sm:w-2/3">
				<div class="logoContainer bg-white">
					<img src="logo-extended.png" alt="logo" class="logo-image" />
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	h1 {
		font-size: 56px;
	}

	h2 {
		font-size: xx-large;
	}
	h3 {
		font-size: x-large;
		text-align: center;
	}

	.bannerSubText {
		font-size: x-large;
		background-color: hsl(var(--primary));
		padding: 0px 4px;
	}

	#homeBanner {
		position: relative;
		width: 100%;
		height: 40vh;
		overflow: hidden;
	}

	#homeBanner::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-image: url('/chandalier.avif');
		background-size: cover;
		background-position: center;
		background-repeat: no-repeat;
		filter: brightness(50%);
		z-index: 1;
	}

	.bannerText {
		position: relative;
		z-index: 2;
		color: white;
		text-align: center;
		padding: 1em;
	}

	.carousel img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		aspect-ratio: 4 / 3;
	}

	.logoContainer {
		/* padding: 0.5rem; */
		aspect-ratio: 1/1; /* Ensures the container maintains a square aspect ratio */
		border: 0.25rem solid hsl(var(--primary));
		border-radius: 50%;
		text-align: center;
		box-shadow:
			0 4px 6px rgba(0, 0, 0, 0.5),
			0 4px 4px rgba(0, 0, 0, 0.5);

		display: flex;
		justify-content: center; /* Centers the image horizontally */
		align-items: center; /* Centers the image vertically */
	}

	.logo-image {
		max-width: 100%;
		max-height: 100%;
		object-fit: fill;
		border-radius: 50%;
	}

	@media (max-width: 1280px) {
		h1 {
			font-size: xxx-large;
		}

		h2 {
			font-size: xx-large;
		}
		h3 {
			font-size: large;
		}
	}

	@media (max-width: 640px) {
		h1 {
			font-size: larger;
			font-weight: 600;
		}

		h2 {
			font-size: x-large;
		}

		h3 {
			font-size: medium;
		}

		.bannerSubText {
			font-size: medium;
		}

		#homeBanner {
			height: 25vh;
		}

		.bannerText {
			padding: 0.5em;
		}
	}
</style>
