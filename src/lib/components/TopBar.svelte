<script>
	import { page } from '$app/stores';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	$: activeUrl = $page.url.pathname;
	const activeClass =
		'text-tertiary font-bold dark:text-dark-tertiary hover:text-primary hover:dark:text-dark-primary';
	const nonActiveClass =
		'text-primary dark:text-dark-primary hover:text-tertiary hover:dark:text-dark-tertiary';
</script>

<Navbar class="bg-background dark:bg-dark-background">
	<NavBrand class="mr-8" href="/">
		<img src="/logo.jpg" class="mr-3 h-12 w-12 rounded" alt="logo" />
		<span
			class="text-primary dark:text-dark-primary hover:text-tertiary hover:dark:text-dark-tertiary self-center whitespace-nowrap text-xl font-semibold"
			>Logo Text</span
		>
	</NavBrand>
	<NavUl {activeUrl} {activeClass} {nonActiveClass}>
		<NavLi href="/">Home</NavLi>
		<NavLi href="/about">About Us</NavLi>
		<NavLi href="/contact">Contact</NavLi>
	</NavUl>
	<NavHamburger />
</Navbar>
