<script>
	import { Section, News, HeroHeader, HeroBody } from 'flowbite-svelte-blocks';
	import { Button } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';
</script>

<svelte:head>
	<title>Holon</title>
	<meta name="description" content="About this app" />
</svelte:head>

<Section name="heroVisual">
	<div class="mr-auto place-self-center lg:col-span-7">
		<HeroHeader
			h1Class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white"
			pClass="max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400"
		>
			<svelte:fragment slot="h1">Payments tool for software companies</svelte:fragment>
			<svelte:fragment slot="paragraph"
				>From checkout to global sales tax compliance, companies around the world use Flowbite to
				simplify their payment stack.</svelte:fragment
			>
			<a href="/"
				><Button size="xl" color="red" class="mr-3 inline-flex items-center justify-center"
					>Get started<ArrowRightOutline size="md" class="-mr-1 ml-2" /></Button
				>
			</a>
			<a href="/"
				><Button color="light" size="xl" class="inline-flex items-center justify-center"
					>Speak to Sales</Button
				>
			</a>
		</HeroHeader>
	</div>
	<div class="hidden lg:col-span-5 lg:mt-0 lg:flex">
		<img
			src="https://firebasestorage.googleapis.com/v0/b/holonconsulting-9064d.appspot.com/o/main_bg.jpg?alt=media&token=4f37d5c1-342f-4887-9998-93c413fe8c49"
			alt="mockup"
		/>
	</div>
</Section>
