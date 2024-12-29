<script>
	import { browser } from '$app/environment';
	import { AnimatedCounter } from '@benzara/svelte-animated-counter';
	import Carousel from '$lib/components/Carousel.svelte';
	import Reviews from '$lib/components/Reviews.svelte';
</script>

{#if browser}
	<Carousel />
{/if}
<div class="mx-2">
	<p class="my-2">
		Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer consequat sem eget enim
		venenatis, non pharetra lacus tempor. Curabitur suscipit magna scelerisque, dapibus lectus sit
		amet, gravida justo. Nullam imperdiet ultricies quam, id blandit orci condimentum id. Nam
		commodo sodales porttitor. Ut blandit ante at nibh accumsan, dictum luctus quam imperdiet.
	</p>
	<div class="text-center">
		In <AnimatedCounter
			values={Array.from({ length: 5 }, (_, i) => (new Date().getFullYear() + i).toString())}
			interval={100}
			direction="down"
			loop={false}
			ease="ease-in-out"
			class="text-lg font-bold"
		/> we had
		<AnimatedCounter
			values={Array.from({ length: 101 }, (_, i) => (900 + i).toString())}
			interval={20}
			direction="up"
			loop={false}
			ease="ease-in-out"
			class="text-lg font-bold"
		/> happy users.
	</div>
	<Reviews />
	<p>
		Aliquam dignissim nibh et tellus aliquet, in fermentum odio molestie. Vivamus mollis cursus nisi
		vitae iaculis. Curabitur sit amet ligula ante. Phasellus tristique lorem nec tortor volutpat,
		sed feugiat orci imperdiet. Vestibulum faucibus eleifend elit rutrum gravida. Maecenas euismod
		vulputate neque, eu dapibus lorem varius nec. Mauris euismod scelerisque dolor vitae volutpat.
		Donec convallis ut elit eu venenatis. Pellentesque pretium molestie lacus eget ullamcorper. Nunc
		maximus dui quis est ullamcorper, sit amet pharetra justo luctus. In pellentesque nibh at dui
		suscipit condimentum. Sed et augue iaculis, faucibus neque vel, fermentum eros. Curabitur vel
		sodales est, pulvinar malesuada mi. Integer libero dui, rutrum sed consectetur ac, facilisis
		eget est. Maecenas arcu orci, rutrum eget feugiat id, convallis in nisi. Proin dictum nulla ac
		metus iaculis tincidunt. Praesent enim ex, viverra vitae diam ut, luctus faucibus turpis.
	</p>
	<p>
		Integer egestas euismod orci sit amet tempus. Curabitur odio libero, cursus a odio non, gravida
		aliquam lorem. Vestibulum mollis mi at urna tristique pharetra. Pellentesque tristique ipsum
		nisl, ut pretium justo bibendum at. Aenean non nunc non orci sodales vehicula. Vivamus cursus
		lacus tortor, et vulputate odio congue eu. Curabitur condimentum libero quis rutrum gravida.
		Mauris neque orci, fermentum vel elit non, vehicula mattis neque. Quisque finibus nisl justo, ac
		efficitur risus consectetur ultricies. Nam vel faucibus felis. Nulla a convallis sem. Aenean
		vestibulum mi vitae accumsan volutpat. Nullam sapien turpis, lacinia eleifend felis id, vehicula
		varius nunc. Morbi iaculis leo a est suscipit dapibus. Ut efficitur sem ligula, id finibus
		turpis auctor luctus. Aliquam commodo tellus mi, vitae tincidunt metus faucibus at. Nam a nisi
		consequat, blandit mauris at, elementum mi. Pellentesque nec pulvinar ipsum, non aliquet erat.
		Nullam lobortis fermentum augue, ut sagittis odio accumsan eu. Cras id risus nec elit posuere
		lacinia eu et purus. Curabitur purus arcu, condimentum et est ac, auctor tincidunt enim.
	</p>
	<p>
		Vestibulum vehicula, turpis tempor aliquet aliquet, risus risus cursus risus, egestas rutrum sem
		orci vitae nulla. Praesent congue mauris ut facilisis imperdiet. Duis pretium sit amet purus eu
		consequat. Mauris vel nulla lacus. Pellentesque feugiat, libero a laoreet gravida, nulla lacus
		vulputate arcu, nec pellentesque nibh dolor vel sem. Vivamus ut ornare augue. Sed libero risus,
		efficitur quis magna id, rhoncus gravida sapien. In in efficitur nisl, vitae pretium odio. Sed
		non nibh quis ante euismod efficitur posuere id mi. Aliquam ornare odio rutrum purus egestas
		ultrices. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia
		curae; In eu urna lacus. Vestibulum purus nisi, fringilla auctor laoreet vel, cursus et nunc.
		Fusce viverra mattis imperdiet. Aenean fringilla mi a dictum dapibus. Ut porta sagittis
		fermentum. Vestibulum sollicitudin posuere erat ac dignissim.
	</p>
</div>
