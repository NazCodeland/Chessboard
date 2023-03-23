<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	export let color: string;
	export let xy: string | number;

	const dispatch = createEventDispatcher();
	function handleCLick() {
		// dispatch('coordinates', {
		// 	xy: {
		// 		x: 2,
		// 		y: 2
		// 	}
		// });
		console.log(xy);
	}
</script>

<button value={xy} on:click={handleCLick} class="w-full h-full cursor-default {color}">
	<slot /></button
>

<style>
</style>
