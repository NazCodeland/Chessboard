<script>
	import Square from '../lib/elements/Square.svelte';
	import QueenLight from '../lib/SVGs/QueenLight.svelte';
	import QueenDark from '../lib/SVGs/QueenDark.svelte';
	import Row from '../lib/components/Row.svelte';
	import File from '../lib/elements/File.svelte';
	import Rank from '../lib/elements/Rank.svelte';
</script>

<div class="grid place-items-center">
	<div class="flex">
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
	</div>
	<div class="flex">
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
	</div>
</div>

<style>
	.gridLayout {
		display: grid;
		gap: 1rem;
		/* grid-template-columns: repeat(8, 130px); */
		/* grid-template-rows: repeat(8, 130px); */
		/* grid-template-areas:
			'. a b c d e f g h .'
			'a1 b1 c1 d1 f1 g1 h1'
			'2 . . . . . . . . 2'
			'3 . . . . . . . . 3'
			'4 . . . . . . . . 4'
			'5 . . . . . . . . 5'
			'6 . . . . . . . . 6'
			'7 . . . . . . . . 7'
			'8 . . . . . . . . 8'
			'. k b c d e f g h .'; */
	}
</style>
