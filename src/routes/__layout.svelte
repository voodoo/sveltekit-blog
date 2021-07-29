<script>
	import Nav from '$lib/Nav.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		const btn = document.querySelector('.mobile-menu-button');
		const sidebar = document.querySelector('.sidebar');

		// add our event listener for the click
		btn.addEventListener('click', () => {
			sidebar.classList.toggle('-translate-x-full');
		});
	});
	// grab everything we need
</script>

<div class="relative min-h-screen md:flex">
	<!-- mobile menu bar -->
	<div class="bg-gray-800 text-gray-100 flex justify-between md:hidden">
		<!-- logo -->
		<a href="/" class="block p-4 text-white font-bold">Hybrid Hero</a>

		<!-- mobile menu button -->
		<button class="mobile-menu-button p-4 focus:outline-none focus:bg-gray-700">
			<svg
				class="h-5 w-5"
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M4 6h16M4 12h16M4 18h16"
				/>
			</svg>
		</button>
	</div>

	<!-- sidebar -->
	<div
		class="sidebar bg-gray-800 text-blue-100 w-64 space-y-6 py-7 px-2 absolute inset-y-0 left-0 transform -translate-x-full md:relative md:translate-x-0 transition duration-200 ease-in-out"
	>
		<!-- logo -->
		<a href="/" class="text-white flex items-center space-x-2 px-4">
			<img src="/assets/img/hero2.png" width="34" height="34" alt="hybrid hero">
			<!-- <svg
				class="w-8 h-8"
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"
				/>
			</svg> -->
			<span class="text-2xl font-extrabold">Hybrid Hero</span>
		</a>

		<!-- nav -->
		<Nav />
	</div>

	<!-- content -->
	<div class="flex-1 p-10 text-2xl font-bold">
		<slot />
	</div>
</div>


<style>

:global(ul) {
		list-style: disc !important;
	}
	:global(li) {
		margin-left: 32px !important;
		padding-left: 12px !important;
	}	
	:global(h4){
		color: teal;
	}
	:global(h1){
		color: rgb(2, 68, 68);
		border-bottom: 2px solid #ccc;
	}	
	
	@tailwind base;
	@tailwind components;
	@tailwind utilities; 
</style>
