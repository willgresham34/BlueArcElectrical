<script lang="ts">
	// import * as Carousel from '$lib/components/ui/carousel/index.js';
	// import Autoplay from 'embla-carousel-autoplay';
	// import { familyPhotos } from '$lib/familyPhotos';

	// const plugin = Autoplay({ delay: 5000, stopOnInteraction: true });
</script>

<div class="flex h-fit flex-col items-center justify-center">
	<div class="pt-6 text-center">
		<h1 class="bg-primary rounded-lg p-2 text-xl font-semibold text-white shadow-2xl sm:text-3xl">
			About Us
		</h1>
	</div>
	<div class="about-us grid grid-cols-1 gap-4 lg:grid-cols-2">
		<!-- <div class="flex items-center justify-center">
			<img class="team-photo" src="KrissyAndMichael.avif" alt="Our Team" /> 
		</div> -->
		<div class="lg:text-md paragraphs bg-primary flex flex-col gap-4 text-lg shadow-2xl">
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
				laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
				voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
				cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
			</p>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
				laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
				voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
				cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
			</p>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
				laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
				voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
				cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
			</p>

			<p>We look forward to building something great together!</p>
		</div>
	</div>
	<div class="cursive-header flex flex-wrap justify-center text-xl">
		<h1 class="">From My Family To Yours&nbsp;</h1>
		<h1 class="">Thank You For Your Business</h1>
	</div>

	<div class="carousel mb-4">
		<!-- <Carousel.Root plugins={[plugin]}>
			<Carousel.Content>
				{#each familyPhotos as photo}
					<Carousel.Item class=" basis-1/2 sm:basis-1/3 lg:basis-1/4 xl:basis-1/5"
						><img src={`/family/${photo}`} alt="familyPhoto" /></Carousel.Item
					>
				{/each}
			</Carousel.Content>
		</Carousel.Root> -->
	</div>
</div>

<style>
	.cursive-header {
		/* font-family: 'Great Vibes', cursive; */
		font-weight: 600;
		text-align: center;
		margin-top: 2rem;
		margin-bottom: 1rem;
	}
	.about-us {
		padding: 1rem 3rem;
		font-family: Arial, sans-serif;
		color: #333;
		line-height: 1.6;
		max-width: 1500px;
		min-width: 75vw;
	}

	h1 {
		text-align: center;
		color: #2c3e50;
	}

	.team-photo {
		width: 100%;
		object-fit: cover;
		margin: 1rem 0;
		border-radius: 8px;
		aspect-ratio: 1/1;
		max-width: 600px;
	}

	.carousel img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		aspect-ratio: 4 / 3;
	}

	.paragraphs {
		background-color: rgb(69, 84, 93);
		color: white;
		box-shadow:
			0 20px 25px -5px rgb(0 0 0 / 0.1),
			0 8px 10px -6px rgb(0 0 0 / 0.1);
		padding: 1rem;
		border-radius: 5px;
	}
</style>
