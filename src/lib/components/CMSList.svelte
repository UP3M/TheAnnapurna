<script lang="ts">
	import ListCard from './ListCard.svelte';
	import { onMount } from 'svelte';
	import { onValue, ref } from 'firebase/database';
	import { db } from '$lib/scripts/firestore';

	let postss = new Array();

	onMount(() => {
		onValue(ref(db, '/posts'), (s) => {
			if (s.exists()) {
				postss = Object.values(s.val());
			}
		});
	});
</script>

<div class="lg:h-full flex flex-wrap items-center text-gray-600">
	{#each postss as post, i}
		<div class="p-4 lg:w-1/2">
			<ListCard {post} {i} />
		</div>
	{/each}
</div>
