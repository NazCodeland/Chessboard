<script>
	import Square from '$lib/elements/Square.svelte';
	import QueenLight from '$lib/SVGs/QueenLight.svelte';
	import QueenDark from '$lib/SVGs/QueenDark.svelte';
</script>

<Square color={'bg-squareDark'}>
	<QueenDark />
</Square>

<Square color={'bg-squareLight'}>
	<QueenLight />
</Square>

<h1>Welcome to SvelteKit</h1>
<p>
	Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
</p>
