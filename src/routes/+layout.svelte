<script lang="ts">
	import '../app.css';
	let { children } = $props();
	import TopBar from '$lib/components/TopBar.svelte';
</script>

<TopBar />
{@render children()}
<footer class="flex flex-wrap items-center justify-center bg-gray-900 py-4 text-white">
	<ul class="m-2">
		<li>Contact</li>
		<li>Details</li>
		<li>In</li>
		<li>Footer</li>
	</ul>
	<ul class="m-2">
		<li>Contact</li>
		<li>Details</li>
		<li>In</li>
		<li>Footer</li>
	</ul>
	<ul class="m-2">
		<li>Contact</li>
		<li>Details</li>
		<li>In</li>
		<li>Footer</li>
	</ul>
	<p class="text-sm">Website by <a href="https://seanbehan.ca">Sean Behan</a></p>
</footer>
