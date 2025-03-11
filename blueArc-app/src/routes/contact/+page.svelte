<script lang="ts">
	import { Input } from '$lib/components/ui/input/index.js';
	import { Button } from '$lib/components/ui/button/index.js';
	import { Label } from '$lib/components/ui/label/index.js';
	import { Textarea } from '$lib/components/ui/textarea/index.js';
	import {
		Select,
		SelectTrigger,
		SelectContent,
		SelectItem,
		SelectSeparator,
		SelectScrollUpButton,
		SelectScrollDownButton
	} from '$lib/components/ui/select/index.js';
	import type { Selected } from 'bits-ui';
	import { writable } from 'svelte/store';
	import emailjs from '@emailjs/browser';

	let formData = {
		email: '',
		phone: '',
		firstName: '',
		lastName: '',
		contactPreference: '',
		subject: '',
		message: ''
	};

	const handleSubmit = async (event: Event) => {
		event.preventDefault();

		const requiredFields = [
			'email',
			'firstName',
			'lastName',
			'contactPreference',
			'subject',
			'message'
		];
		const missingFields = requiredFields.filter(
			(field) => !formData[field as keyof typeof formData].trim()
		);

		if (missingFields.length > 0) {
			alert(`Please fill out the following required fields: ${missingFields.join(', ')}`);
			return;
		}

		try {
			const response = await emailjs.send(
				'service_BlueArc',
				'template_BlueArc',
				formData,
				'ULLZ_FCOOOT4n6eZa'
			);
			console.log('Email sent successfully:', response);
			formData = {
				email: '',
				phone: '',
				firstName: '',
				lastName: '',
				contactPreference: '',
				subject: '',
				message: ''
			};
			alert('Your message has been sent!');
		} catch (error) {
			console.error('Failed to send email:', error);
			alert('There was an error sending your message.');
		}
	};
</script>

<div>
	<div class=" flex flex-col items-center gap-2 p-4">
		<h1 class="contact bg-primary rounded-xl px-4 py-2 text-white">Contact Us</h1>
	</div>
	<div class="mx-2">
		<div class=" grid grid-cols-1 gap-4 rounded-xl sm:grid-cols-2">
			<!-- left col -->
			<div class="bg-primary grid grid-cols-2 gap-4 rounded-xl p-4 shadow-2xl sm:grid-cols-1">
				<div class="flex flex-col items-center justify-center">
					<div id="phoneIcon">
						<a href="tel:+14049334101" class="text-white" aria-label="Phone">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								x="0px"
								y="0px"
								width="100"
								height="100"
								viewBox="0 0 48 48"
							>
								<path
									fill="#0f0"
									d="M13,42h22c3.866,0,7-3.134,7-7V13c0-3.866-3.134-7-7-7H13c-3.866,0-7,3.134-7,7v22	C6,38.866,9.134,42,13,42z"
								></path><path
									fill="#fff"
									d="M35.45,31.041l-4.612-3.051c-0.563-0.341-1.267-0.347-1.836-0.017c0,0,0,0-1.978,1.153	c-0.265,0.154-0.52,0.183-0.726,0.145c-0.262-0.048-0.442-0.191-0.454-0.201c-1.087-0.797-2.357-1.852-3.711-3.205	c-1.353-1.353-2.408-2.623-3.205-3.711c-0.009-0.013-0.153-0.193-0.201-0.454c-0.037-0.206-0.009-0.46,0.145-0.726	c1.153-1.978,1.153-1.978,1.153-1.978c0.331-0.569,0.324-1.274-0.017-1.836l-3.051-4.612c-0.378-0.571-1.151-0.722-1.714-0.332	c0,0-1.445,0.989-1.922,1.325c-0.764,0.538-1.01,1.356-1.011,2.496c-0.002,1.604,1.38,6.629,7.201,12.45l0,0l0,0l0,0l0,0	c5.822,5.822,10.846,7.203,12.45,7.201c1.14-0.001,1.958-0.248,2.496-1.011c0.336-0.477,1.325-1.922,1.325-1.922	C36.172,32.192,36.022,31.419,35.45,31.041z"
								></path>
							</svg>
						</a>
					</div>

					<h2 class="text-xl text-white">Call Us</h2>
					<a href="tel:+14049334101" class="text-white">(404) 933-4101</a>
				</div>
				<div class=" flex flex-col items-center justify-center">
					<a
						href="https://www.facebook.com/profile.php?id=61571450200141"
						aria-label="Facebook link"
						target="_blank"
						id="facebookIcon"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							x="0px"
							y="0px"
							width="100"
							height="100"
							viewBox="0 0 48 48"
						>
							<linearGradient
								id="Ld6sqrtcxMyckEl6xeDdMa_uLWV5A9vXIPu_gr1"
								x1="9.993"
								x2="40.615"
								y1="9.993"
								y2="40.615"
								gradientUnits="userSpaceOnUse"
								><stop offset="0" stop-color="#2aa4f4"></stop><stop offset="1" stop-color="#007ad9"
								></stop></linearGradient
							><path
								fill="url(#Ld6sqrtcxMyckEl6xeDdMa_uLWV5A9vXIPu_gr1)"
								d="M24,4C12.954,4,4,12.954,4,24s8.954,20,20,20s20-8.954,20-20S35.046,4,24,4z"
							></path><path
								fill="#fff"
								d="M26.707,29.301h5.176l0.813-5.258h-5.989v-2.874c0-2.184,0.714-4.121,2.757-4.121h3.283V12.46 c-0.577-0.078-1.797-0.248-4.102-0.248c-4.814,0-7.636,2.542-7.636,8.334v3.498H16.06v5.258h4.948v14.452 C21.988,43.9,22.981,44,24,44c0.921,0,1.82-0.084,2.707-0.204V29.301z"
							></path>
						</svg>
					</a>
					<h2 class="text-xl text-white">Like our page!</h2>
				</div>
				<div
					class="text-accent-foreground hover:text-accent justify-centers flex flex-col items-center"
				>
					<a
						href="https://www.instagram.com/bluearcelectricllc/"
						target="_blank"
						aria-label="Instagram"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							x="0px"
							y="0px"
							width="100"
							height="100"
							viewBox="0 0 48 48"
						>
							<radialGradient
								id="yOrnnhliCrdS2gy~4tD8ma_Xy10Jcu1L2Su_gr1"
								cx="19.38"
								cy="42.035"
								r="44.899"
								gradientUnits="userSpaceOnUse"
								><stop offset="0" stop-color="#fd5"></stop><stop offset=".328" stop-color="#ff543f"
								></stop><stop offset=".348" stop-color="#fc5245"></stop><stop
									offset=".504"
									stop-color="#e64771"
								></stop><stop offset=".643" stop-color="#d53e91"></stop><stop
									offset=".761"
									stop-color="#cc39a4"
								></stop><stop offset=".841" stop-color="#c837ab"></stop></radialGradient
							><path
								fill="url(#yOrnnhliCrdS2gy~4tD8ma_Xy10Jcu1L2Su_gr1)"
								d="M34.017,41.99l-20,0.019c-4.4,0.004-8.003-3.592-8.008-7.992l-0.019-20	c-0.004-4.4,3.592-8.003,7.992-8.008l20-0.019c4.4-0.004,8.003,3.592,8.008,7.992l0.019,20	C42.014,38.383,38.417,41.986,34.017,41.99z"
							></path><radialGradient
								id="yOrnnhliCrdS2gy~4tD8mb_Xy10Jcu1L2Su_gr2"
								cx="11.786"
								cy="5.54"
								r="29.813"
								gradientTransform="matrix(1 0 0 .6663 0 1.849)"
								gradientUnits="userSpaceOnUse"
								><stop offset="0" stop-color="#4168c9"></stop><stop
									offset=".999"
									stop-color="#4168c9"
									stop-opacity="0"
								></stop></radialGradient
							><path
								fill="url(#yOrnnhliCrdS2gy~4tD8mb_Xy10Jcu1L2Su_gr2)"
								d="M34.017,41.99l-20,0.019c-4.4,0.004-8.003-3.592-8.008-7.992l-0.019-20	c-0.004-4.4,3.592-8.003,7.992-8.008l20-0.019c4.4-0.004,8.003,3.592,8.008,7.992l0.019,20	C42.014,38.383,38.417,41.986,34.017,41.99z"
							></path><path
								fill="#fff"
								d="M24,31c-3.859,0-7-3.14-7-7s3.141-7,7-7s7,3.14,7,7S27.859,31,24,31z M24,19c-2.757,0-5,2.243-5,5	s2.243,5,5,5s5-2.243,5-5S26.757,19,24,19z"
							></path><circle cx="31.5" cy="16.5" r="1.5" fill="#fff"></circle><path
								fill="#fff"
								d="M30,37H18c-3.859,0-7-3.14-7-7V18c0-3.86,3.141-7,7-7h12c3.859,0,7,3.14,7,7v12	C37,33.86,33.859,37,30,37z M18,13c-2.757,0-5,2.243-5,5v12c0,2.757,2.243,5,5,5h12c2.757,0,5-2.243,5-5V18c0-2.757-2.243-5-5-5H18z"
							></path>
						</svg>
					</a>
					<h2 class="text-center text-xl text-white">Follow us on Instagram!</h2>
				</div>
			</div>
			<!-- right col -->
			<div class=" rounded-lg border bg-white p-2 shadow-2xl">
				<form on:submit={handleSubmit} class="">
					<div class="form-body flex flex-col gap-3 p-2">
						<div class="grid grid-cols-1 gap-2 lg:grid-cols-2">
							<div>
								<Label for="email">Email</Label>
								<Input
									type="email"
									id="email"
									placeholder="example@gmail.com"
									bind:value={formData.email}
								/>
							</div>
							<div>
								<Label for="phone">Phone # <span class="text-xs">(Optional)</span></Label>
								<Input
									type="text"
									id="phone"
									placeholder="123-456-7890"
									bind:value={formData.phone}
								/>
							</div>
						</div>
						<div class="flex w-full gap-2">
							<div class="w-1/2">
								<Label for="firstName">First Name</Label>
								<Input
									type="text"
									id="firstName"
									placeholder="John"
									bind:value={formData.firstName}
								/>
							</div>
							<div class="w-1/2">
								<Label for="lastName">Last Name</Label>
								<Input type="text" id="lastName" placeholder="Doe" bind:value={formData.lastName} />
							</div>
						</div>
						<div>
							<Label for="contactPreference">Contact Preference</Label>
							<Select bind:value={formData.contactPreference} type="single">
								<SelectTrigger>
									{formData.contactPreference ? formData.contactPreference : 'Select an option'}
								</SelectTrigger>
								<SelectContent>
									3 <SelectItem value="Email">Email</SelectItem>
									<SelectItem value="Phone">Phone</SelectItem>
									<SelectItem value="Text Message">Text Message</SelectItem>
								</SelectContent>
							</Select>
						</div>

						<div>
							<Label for="subject">Subject</Label>
							<Input type="text" id="subject" placeholder="" bind:value={formData.subject} />
						</div>
						<div>
							<Label for="message">Message</Label>
							<Textarea id="message" placeholder="" class="h-56" bind:value={formData.message} />
						</div>

						<Button type="submit" class="bg-primary text-lg font-semibold text-white">Send</Button>
					</div>
				</form>
			</div>
		</div>
	</div>
</div>

<style>
	.contact {
		font-size: 40px;
	}
</style>
