<script lang="ts">
</script>

<div class="flex h-fit flex-col items-center justify-center">
	<div class="pt-6 text-center">
		<h1 class="bg-primary rounded-lg p-2 text-xl font-semibold text-white shadow-2xl sm:text-3xl">
			About Us
		</h1>
	</div>
	<div class="about-us grid grid-cols-1 gap-4 lg:grid-cols-2">
		<div class="flex items-center justify-center">
			<img class="team-photo" src="Dario_F.avif" alt="Our Team" />
		</div>
		<div class="lg:text-md paragraphs bg-primary flex flex-col gap-4 text-lg shadow-2xl">
			<p>
				At Blue Arc Electrical, we are a fresh and innovative electrical company founded by two
				lifelong friends who share a passion for quality craftsmanship and reliable service. With
				years of industry experience, we built Blue Arc Electrical to provide expert electrical
				solutions for homeowners and businesses alike. From wiring and panel upgrades to lighting
				installations and EV charger setups, we are committed to delivering safe, efficient, and
				modern electrical systems that meet the evolving needs of our customers. Whether you need to
				upgrade an outdated electrical panel or install energy-efficient lighting, we ensure every
				project is completed with precision and professionalism.
			</p>
			<p>
				Customer satisfaction is the foundation of our business. We take pride in offering
				personalized service, tailoring solutions to fit each client’s specific needs. Our
				commitment to safety, innovation, and attention to detail sets us apart in the industry. As
				a locally owned and operated company, we value the relationships we build with our customers
				and the community. Whether you’re renovating your home, upgrading your commercial space, or
				installing an EV charging station, Blue Arc Electrical is ready to power your project with
				expertise and reliability.
			</p>
			<p>We look forward to making your dream a reality!</p>
		</div>
	</div>
</div>

<style>
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
	}

	.team-photo {
		width: 100%;
		object-fit: cover;
		margin: 1rem 0;
		border-radius: 8px;
		aspect-ratio: 1/1;
		max-width: 600px;
	}

	.paragraphs {
		color: white;
		box-shadow:
			0 20px 25px -5px rgb(0 0 0 / 0.1),
			0 8px 10px -6px rgb(0 0 0 / 0.1);
		padding: 1rem;
		border-radius: 5px;
	}
</style>
