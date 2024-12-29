<script lang="ts">
	import { onMount } from 'svelte';
	import { Carousel } from 'flowbite';
	import type { CarouselItem, CarouselOptions, CarouselInterface } from 'flowbite';
	import type { InstanceOptions } from 'flowbite';

	onMount(() => {
		const carouselElement: HTMLElement =
			document.getElementById('carousel') ?? document.createElement('div');

		const items: CarouselItem[] = [
			{
				position: 0,
				el: document.getElementById('carousel-item-1') ?? document.createElement('div')
			},
			{
				position: 1,
				el: document.getElementById('carousel-item-2') ?? document.createElement('div')
			}
		];

		const options: CarouselOptions = {
			defaultPosition: 0,
			interval: 10000
		};

		const instanceOptions: InstanceOptions = {
			id: 'carousel',
			override: true
		};

		const carousel: CarouselInterface = new Carousel(
			carouselElement,
			items,
			options,
			instanceOptions
		);

		carousel.cycle();
	});
</script>

<div id="carousel" class="relative w-full">
	<div class="relative h-56 overflow-hidden sm:h-64 xl:h-80 2xl:h-96">
		<div id="carousel-item-1" class="hidden duration-700 ease-in-out">
			<img
				src="https://images.pexels.com/photos/6829543/pexels-photo-6829543.jpeg"
				class="absolute left-1/2 top-1/2 block w-full -translate-x-1/2 -translate-y-1/2"
				alt="..."
			/>
		</div>
		<div id="carousel-item-2" class="hidden duration-700 ease-in-out">
			<img
				src="https://images.pexels.com/photos/29161722/pexels-photo-29161722/free-photo-of-assorted-fresh-pastries-on-wooden-board.jpeg"
				class="absolute left-1/2 top-1/2 block w-full -translate-x-1/2 -translate-y-1/2"
				alt="..."
			/>
		</div>
	</div>
</div>
