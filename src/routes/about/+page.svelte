<script>
	import { News, HeroHeader, HeroBody, Section } from 'flowbite-svelte-blocks';
	import { Button } from 'flowbite-svelte';
	import { ArrowRightSolid } from 'flowbite-svelte-icons';

	import Youtube from '../utils/icons/Youtube.svelte';
	import Reddit from '../utils/icons/Reddit.svelte';
	import ProductHunt from '../utils/icons/ProductHunt.svelte';
</script>

<Section name="heroDefault">
	<News>
		<span class="text-xs bg-primary-600 rounded-full text-white px-4 py-1.5 mr-3">New</span>
		<span class="text-sm font-medium">Flowbite is out! See what's new</span>
	</News>
	<HeroHeader>
		<svelte:fragment slot="h1">We invest in the world’s potential</svelte:fragment>
		<svelte:fragment slot="paragraph"
			>Here at Flowbite we focus on markets where technology, innovation, and capital can unlock
			long-term value and drive economic growth.</svelte:fragment
		>
	</HeroHeader>

	<div
		class="flex flex-col mb-8 lg:mb-16 space-y-4 sm:flex-row sm:justify-center sm:space-y-0 sm:space-x-4"
	>
		<a href="/">
			<Button size="lg" color="red">
				Learn more <ArrowRightSolid size="md" class="ml-2 -mr-1" />
			</Button>
		</a>
		<a href="/">
			<Button size="lg" color="light">
				<!-- <VideoSolid size="xs" class="mr-2 -ml-1" /> -->
				Watch video
			</Button>
		</a>
	</div>
	<HeroBody>
		<svelte:fragment slot="head">FEATURED IN</svelte:fragment>

		<div class="flex flex-wrap justify-center items-center mt-8 text-gray-500 sm:justify-between">
			<a href="/" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
				<Youtube />
			</a>
			<a href="/" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
				<ProductHunt />
			</a>
			<a href="/" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
				<Reddit />
			</a>
		</div>
	</HeroBody>
</Section>s
