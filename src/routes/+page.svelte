<script lang="ts">
	const features = [
		{
			title: 'Krupuk Kulit Ikan',
			icon: 'pouchex'
			// description: 'Choose the best location and your favorite workspace easily.'
		},
		{
			title: 'Keripik Tempe',
			icon: 'pouchex'
			// description: 'Know more about your new place and Get the best recomendation for your business from our team.'
		},
		{
			title: 'Sambal Kering Ebi',
			icon: 'pouchex'
			// description: 'We provide service that can deal with laws and regulations that the startup needs to comply.'
		},
		{
			title: 'Sambal kering Teri',
			icon: 'pouchex'
			// description: 'Offer subscriptions or one-time purchases. Accept credit cards & PayPal.'
		},
		{
			title: 'Keripik Tempe Flavored',
			icon: 'pouchex'
			// description: 'Know what your customer likes & how your product fit them.'
		},
		{
			title: 'Kerupuk Kulit Ikan Flavored',
			icon: 'pouchex'
			// description:	'Upload your free space in our platform and we will organize it for you.'
		}
	];
</script>

<!-- <svelte:head>
	<title>See You Again</title>
	<meta name="robots" content="" />
	<html lang="en" />
</svelte:head> -->

<!-- Hero Section -->
<section
	class="flex flex-col min-h-screen bg-slate-600 text-white bg-center bg-cover bg-blend-overlay bg-fixed bg-black/25"
	style="background-image: url(../images/ikan.jpg)"
>
	<!-- Hero Section Content -->
	<div class="flex-1 flex items-center">
		<div class="text-center mx-auto">
			<h1 class="text-6xl font-semibold">The Annapurna Baliexpo</h1>
			<h2 class="text-xl font-semibold">
				The expert of Indonesia Micro, Small Medium Enterprise products
			</h2>
			<button class="mt-10 w-1/3 outline bg-yellow-500 font-semibold"
				><a href="/Workspace">Our Products</a></button
			>
			<button class="mx-10 w-1/3 outline bg-black"
				><a href="mailto:theannapurnabaliexpo@gmail.com">Contact Us</a></button
			>
		</div>
	</div>
</section>

<section class="p-10 text-white bg-gradient-to-b via-yellow-500 from-brightRed">
	<div class="max-w-screen-xl mx-auto">
		<div class="md:flex items-center space-x-24">
			<div class="flex flex-col md:w-1/2">
				<div class="flex flex-col space-y-4">
					<h2 class="text-4xl font-bold font-heading">
						Making a Difference Millions Develop Superior
					</h2>
					<p class="text-justify">
						Our motto means helping various Micro, Small, Medium Enterprise (MSME) products from
						various different classes, such as small and medium micro classes, will always work hand
						in hand to grow and develop rapidly together.
					</p>
				</div>
			</div>
			<div class="relative w-1/2">
				<img
					src="https://pluspng.com/img-png/png-travel-how-to-market-a-travel-and-tourism-outlet-826.png"
					class="md:scale-110 object-bottom"
					alt="expansion"
				/>
			</div>
		</div>
	</div>
</section>

<section class="py-20">
	<div class="max-w-screen-lg mx-auto">
		<div class="flex flex-col justify-center text-center">
			<div class="flex flex-col space-y-3">
				<h2 class="text-4xl font-bold font-heading">Our Products</h2>
				<p>Balinese Authentic Snacks and Sauce</p>
			</div>
			<div class="flex justify-center mt-12 space-x-8">
				<button class="w-1/4 primary"><a href="/Workspace">See Our Products</a></button>
				<button class="w-1/4 outline bg-black"
					><a href="mailto:theannapurnabaliexpo@gmail.com">Contact Us</a></button
				>
			</div>
		</div>
		<div class="grid grid-cols-3 gap-12 mt-10">
			{#each features as feature}
				<div
					class="flex flex-col p-4 space-y-3 hover:shadow-xl transition duration-300 cursor-pointer"
				>
					<img
						src={`/icons/${feature.icon}.png`}
						class="transform transition duration-300 hover:rotate-12"
						alt={feature.title}
					/>
					<h5 class="font-bold font-heading text-center">{feature.title}</h5>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="p-10 py-20 text-white bg-black">
	<div class="flex flex-col max-w-screen-xl mx-auto space-y-20">
		<div class="flex flex-col justify-center">
			<h3 class="text-4xl font-bold text-center font-heading">Benefits of Our Products</h3>
		</div>

		<div class="md:flex md:space-x-24 object-center">
			<div class="relative flex md:w-1/2 w-3/5 h-40 md:h-full">
				<img src="/images/tempe.jpg" class="w-full h-full object-center" alt="kripik tempe" />
			</div>
			<div class="flex flex-col justify-center md:w-1/2 space-y-6">
				<h4 class="text-2xl font-semibold">Keripik Tempe (Soybean Cake Chips)</h4>
				<p class="text-justify">
					Based on the Ministry of Health Indonesia , Keripik Tempe has some benefits :
				</p>
				<ul class="marker:text-sky-400 list-disc pl-5 space-y-3">
					<li>Maintaining blood sugar stability is the benefit of the high fiber content.</li>
					<li>
						Preventing the risk of cardiovascular system disease is the benefit of high content of
						calcium and thiamine.
					</li>
					<li>
						Helping and increasing blood clotting is a benefit from the high content of calcium.
					</li>
					<li>
						Minimizing the occurrence of stroke is the benefit of the high content of calcium and
						phosphorus.
					</li>
					<li>
						Maintaining and increasing the production of hemoglobin is a benefit of the high iron
						content.
					</li>
					<li>Balancing the level of blood acidity is a benefit of high calcium content.</li>
					<li>Reducing the risk of anemia is a benefit of the high iron content.</li>
				</ul>
				<div class="flex space-x-3 cursor-pointer group">
					<a href="/Workspace">
						<p class="transition font-heading group-hover:font-bold">See Our Product</p>
						<img
							src="/icons/arrow.svg"
							class="transition transform group-hover:translate-x-1"
							alt="Arrow Icon"
						/>
					</a>
				</div>
			</div>
		</div>

		<div class="md:flex md:space-x-24">
			<div class="relative flex md:w-1/2 w-3/5 h-40 md:h-full justify-center items-center">
				<img src="/images/ikan2.jpg" class="w-full h-full" alt="kerupuk ikan" />
			</div>
			<div class="flex flex-col justify-center md:w-1/2 space-y-6">
				<h5 class="text-3xl font-semibold">
					Kerupuk KulitIkan Khas Bali (Balinese Fish Skin Crackers)
				</h5>
				<p class="text-justify">
					Based on the Ministry of Health Indonesia ,Kerupuk Kulit Ikan has some benefits :
				</p>
				<p class="text-justify">
					High Nutrition ( Protein, Omega-3 fatty acids, Vitamin D, Vitamin E, Iodine, Selenium,
					Taurine)
				</p>
				<ul class="marker:text-sky-400 list-disc pl-5 space-y-3">
					<li>
						Protein : Fish Skin has protein to boost our body to create new cell and tissue in our
						body, maintain our zinc, and keep our health maintain
					</li>
					<li>
						Omega-3 fatty acids : Reduce inflammation, maintain the heart healthy, stabilize the
						blood pressure, reduce the brain disease, help to maintain the healthy of pregnancy and
						the fetus.
					</li>
					<li>Vitamin D : Help to maintain our bones healthy,</li>
					<li>Vitamin E : Maintain our skin healthy</li>
					<li>Iodine : to make maintain thyroid hi</li>
					<li>Selenium : help to boost immune function, improve the hair and the skin healthy</li>
					<li>Taurine : improve the heart and the brain fat levels</li>
				</ul>
				<div class="flex space-x-3 cursor-pointer group">
					<a href="/Workspace">
						<p class="transition font-heading group-hover:font-bold">See Our Product</p>
						<img
							src="/icons/arrow.svg"
							class="transition transform group-hover:translate-x-1"
							alt="Arrow Icon"
						/>
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- <section class="pt-20 pb-40 text-white bg-black">
	<div class="flex flex-col max-w-screen-lg mx-auto">
		<div class="flex flex-col space-y-3 text-center">
			<h6 class="text-4xl font-bold font-heading">Start your own business today</h6>
			<p>Consistent quality and experience across all platforms and devices.</p>
		</div>
		<div class="flex justify-center space-x-8 mt-14">
			<button class="w-1/4 secondary"><a href="/Workspace">Start Find Workspace</a></button>
			<button class="w-1/4 outline bg-black"><a href="mailto:theannapurnabaliexpo@gmail.com">Contact Us</button>
			
		</div>
	</div>
</section> -->

<section class="p-10 pt-20 pb-32">
	<div class="flex flex-col justify-center space-y-3 text-center">
		<h7 class="text-4xl font-bold font-heading">Our Partnership</h7>
	</div>

	<div
		class="flex flex-col md:flex-row justify-center md:overflow-hidden mt-10 space-y-6 space-x-10"
	>
		<div class="flex justify-center md:space-x-8">
			<img
				src="https://th.bing.com/th/id/OIP.EHEdGmMaCuL9i8WgVU4_uwHaEq?pid=ImgDet&rs=1"
				alt="pnm"
				class="w-[360px] h-[180px]"
			/>
		</div>
		<div class="flex justify-center md:space-x-8">
			<img src="/images/tempego.png" alt="TempeGo" class="w-[360px] h-[180px]" />
		</div>
		<div class="flex justify-center md:space-x-8">
			<img src="/images/ikanprod.png" alt="partner kulit Ikan" class="w-[360px] h-[180px]" />
		</div>
	</div>
</section>

<style lang="postcss" global>
	button {
		@apply px-6 py-3 font-sans rounded-full outline-none transition duration-300;
	}
	button.primary {
		@apply bg-primary text-white hover:bg-blue-700;
	}
	button.outline {
		@apply border-white text-white border-[1px] hover:bg-white hover:text-black;
	}
	button.secondary {
		@apply bg-white text-black hover:bg-neutral-100;
	}
</style>
