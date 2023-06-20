<script lang="ts">
	import CMSList from '$lib/components/CMSList.svelte';
    import authStore from '../../routes/stores/authStore';
</script>

<!-- <svelte:head>
	<title>Find Your Dream Workspace</title>
    <meta name="description" content="We have the best workspace around the world" />
	<meta name="robots" content="" />
	<html lang="en" />
</svelte:head> -->
<section
	class="min-h-screen text-white bg-center bg-cover bg-blend-overlay bg-fixed bg-black/60"
	style="background-image: url(https://cmkt-image-prd.freetls.fastly.net/0.1.0/ps/3683855/1820/1213/m1/fpnw/wm1/krqyfhubd7oft9ct47vf0c4iqejohkp7flkbgbunlmmgg57f8q5om1yzmga7jaod-.jpg?1512398578&s=7dcf9d0943f23852b83ad73f84e51e40);"
>
	<div class="text-center mb-5">
		<h1 class="text-4xl md:text-6xl text-white-700 font-semibold">Balinese Authentic</h1>
		<h2 class="text-2xl md:text-4xl">Snacks and Sauce</h2>
	</div>
    {#if $authStore.isLoggedIn}
        <button class="py-4 text-sm font-bold text-white uppercase bg-teal-500 rounded-sm px-14 hover:bg-blue-600"><a href="/Create">Add Item</a></button>
    {/if}
	<CMSList />
</section>
