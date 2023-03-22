<script>
	import Square from '../elements/Square.svelte';
</script>

<div class="rowLayout gap-4">
	<Square color={'bg-squareLight'}>
		<slot name="a1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="b1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="c1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="d1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="e1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="f1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="g1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="h1" />
	</Square>
	<!--  -->
	<Square color={'bg-squareLight'}>
		<slot name="a1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="b1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="c1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="d1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="e1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="f1" />
	</Square>
	<Square color={'bg-squareLight'}>
		<slot name="g1" />
	</Square>
	<Square color={'bg-squareDark'}>
		<slot name="h1" />
	</Square>
</div>

<style>
	.rowLayout {
		display: grid;
		grid-auto-flow: column;
		grid-template-columns: repeat(8, 1fr);
		grid-template-rows: repeat(8, 1fr);
		gap: 1rem;
	}
</style>
