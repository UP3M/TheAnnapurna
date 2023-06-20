<script lang="ts">
	import { goto } from '$app/navigation';
	import authStore from '../../routes/stores/authStore';
	import { onMount } from 'svelte';

	async function logout() {
		authStore.set({
			isLoggedIn: false,
			firebaseController: false
		});
		goto('/');
	}

	let isMenuOpen = false;
	let navLinks;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	onMount(() => {
		navLinks = document.querySelector('.nav-links');
	});
</script>

<nav
	class="fixed top-0 left-0 z-[999] flex justify-between items-center w-full sticky top-0 w-full bg-gradient-to-r from-yellow-500 via-purple-500 to-pink-500 text-white"
>
	<div>
		<img src="/logo.png" alt="Screeno Logo" class="w-20 h-20" />
	</div>
	<div
		class="hidden md:static md:absolute md:min-h-fit md:min-h-[60vh] md:w-auto w-full md:flex md:mx-20 items-center px-5"
	>
		<ul class="flex md:flex-row flex-col md:items-center md:gap-[4vw] gap-8 text-bold">
			<li>
				<a class="hover:text-gray-500" href="/">Dashboard</a>
			</li>
			<li>
				<a class="hover:text-gray-500" href="/Workspace">Products</a>
			</li>
			<li>
				<a class="hover:text-gray-500" href="/About">About Us</a>
			</li>
		</ul>
	</div>
	<div class="hidden md:flex items-center gap-6 mx-10 my-5">
		{#if $authStore.isLoggedIn}
			<button
				class="bg-[#a6c1ee] text-white px-5 py-2 rounded-50% hover:bg-[#87acec]"
				on:click={logout}>Logout</button
			>
		{:else}
			<button class="bg-[#a6c1ee] text-white px-5 py-2 rounded-50% hover:bg-[#87acec]"
				><a href="/Login">Login</a></button
			>
		{/if}
	</div>

	<div class="md:hidden">
		<button class="text-white focus:outline-none" on:click={toggleMenu}>
			<div>
				<img
					src={isMenuOpen ? '/icons/close.png' : '/icons/menu.png'}
					class="w-10 h-10"
					alt="menubar"
				/>
			</div>
		</button>
	</div>

	<div
		class="md:flex md:items-center md:w-auto w-1/4"
		style="display: {isMenuOpen ? 'block' : 'none'}"
		bind:this={navLinks}
	>
		<ul class="md:flex items-center justify-between text-bold pt-2 md:pt-0">
			<li>
				<a href="/" class="md:p-2 py-1 block">Home</a>
			</li>
			<li>
				<a href="/Workspace" class="md:p-2 py-1 block">Products</a>
			</li>
			<li>
				<a href="/About" class="md:p-2 py-1 block">About</a>
			</li>
		</ul>
		<div class="flex items-center gap-6 my-5">
			{#if $authStore.isLoggedIn}
				<button
					class="bg-[#a6c1ee] text-white px-5 py-2 rounded-50% hover:bg-[#87acec]"
					on:click={logout}>Logout</button
				>
			{:else}
				<button class="bg-[#a6c1ee] text-white px-5 py-2 rounded-50% hover:bg-[#87acec]"
					><a href="/Login">Login</a></button
				>
			{/if}
		</div>
	</div>
</nav>
