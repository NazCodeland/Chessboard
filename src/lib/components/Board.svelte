<script lang="ts">
	import Square from '$lib/elements/Square.svelte';
	import QueenLight from '$lib/SVGs/QueenLight.svelte';
	import QueenDark from '$lib/SVGs/QueenDark.svelte';
	import File from '$lib/elements/File.svelte';
	import Rank from '$lib/elements/Rank.svelte';
	export let size: unknown;
</script>

<div class="gridLayout place-items-center relative">
	<!-- <div class="flex rank-left">
		<Rank rank={1} />
		<Rank rank={2} />
		<Rank rank={3} />
		<Rank rank={4} />
		<Rank rank={5} />
		<Rank rank={6} />
		<Rank rank={7} />
		<Rank rank={8} />
	</div> -->

	<div class="board" style="inline-size:{size}; block-size:{size}">
		<!-- <div class="flex file-top">
			<File text="a" />
			<File text="b" />
			<File text="c" />
			<File text="d" />
			<File text="e" />
			<File text="f" />
			<File text="g" />
			<File text="h" />
		</div> -->

		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />

		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />

		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />

		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />

		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />

		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />

		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />

		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />
		<Square color={'bg-squareDark'} />
		<Square color={'bg-squareLight'} />

		<!-- <div class="flex file-bottom">
			<File text="a" />
			<File text="b" />
			<File text="c" />
			<File text="d" />
			<File text="e" />
			<File text="f" />
			<File text="g" />
			<File text="h" />
		</div> -->
	</div>

	<!-- <div class="flex rank-right">
		<Rank rank={1} />
		<Rank rank={2} />
		<Rank rank={3} />
		<Rank rank={4} />
		<Rank rank={5} />
		<Rank rank={6} />
		<Rank rank={7} />
		<Rank rank={8} />
	</div> -->
</div>

<style>
	.gridLayout {
		display: grid;
		grid-template-areas:
			'.. .. .. ee'
			'rl c  c  rr'
			'.. .. .. ..';
	}

	.board {
		/* grid-area: c;board */
		display: grid;
		grid-template-columns: repeat(8, 1fr);
		grid-template-rows: repeat(8, 1fr);
	}

	.rank-left {
		display: grid;
		grid-area: rl;
	}

	.rank-right {
		display: grid;
		grid-area: rr;
	}
</style>
