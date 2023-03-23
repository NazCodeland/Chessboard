<script lang="ts">
	import Square from '$lib/elements/Square.svelte';
	import QueenLight from '$lib/SVGs/QueenLight.svelte';
	import QueenDark from '$lib/SVGs/QueenDark.svelte';
	import File from '$lib/elements/File.svelte';
	import Rank from '$lib/elements/Rank.svelte';
	export let size: string | number;

	const chessboard = [
		'a1',
		'b1',
		'c1',
		'd1',
		'e1',
		'f1',
		'g1',
		'h1',
		'a2',
		'b2',
		'c2',
		'd2',
		'e2',
		'f2',
		'g2',
		'h2',
		'a3',
		'b3',
		'c3',
		'd3',
		'e3',
		'f3',
		'g3',
		'h3',
		'a4',
		'b4',
		'c4',
		'd4',
		'e4',
		'f4',
		'g4',
		'h4',
		'a5',
		'b5',
		'c5',
		'd5',
		'e5',
		'f5',
		'g5',
		'h5',
		'a6',
		'b6',
		'c6',
		'd6',
		'e6',
		'f6',
		'g6',
		'h6',
		'a7',
		'b7',
		'c7',
		'd7',
		'e7',
		'f7',
		'g7',
		'h7',
		'a8',
		'b8',
		'c8',
		'd8',
		'e8',
		'f8',
		'g8',
		'h8'
	];
</script>

<div style="inline-size:{size}; block-size:{size}" class="gridLayout place-items-center">
	<div class="size h-full flex rank-left">
		<Rank rank={1} />
		<Rank rank={2} />
		<Rank rank={3} />
		<Rank rank={4} />
		<Rank rank={5} />
		<Rank rank={6} />
		<Rank rank={7} />
		<Rank rank={8} />
	</div>

	<div class="size flex w-full file-top">
		<File text="a" />
		<File text="b" />
		<File text="c" />
		<File text="d" />
		<File text="e" />
		<File text="f" />
		<File text="g" />
		<File text="h" />
	</div>

	<!-- {#each chessboard as square}
	{/each} -->

	<!-- board -->
	<div style="inline-size:{size}; block-size:{size}" class="w-full h-full board">
		{#each chessboard as xy, i}
			<!-- if the row rank number is even -->
			{#if xy[1] % 2 === 0}
				<!-- if the index is even -->
				{#if i % 2 === 0}
					<Square {xy} color={'bg-squareDark'} />
				{:else}
					<Square {xy} color={'bg-squareLight'} />
				{/if}

				<!-- if the row rank number is odd -->
			{:else if i % 2 === 0}
				<Square {xy} color={'bg-squareLight'} />
			{:else}
				<Square {xy} color={'bg-squareDark'} />
			{/if}
		{/each}
		<!-- 
		<Square xy="a1" color={'bg-squareLight'} />
		<Square xy="b1" color={'bg-squareDark'} />
		<Square xy="c1" color={'bg-squareLight'} />
		<Square xy="d1" color={'bg-squareDark'} />
		<Square xy="e1" color={'bg-squareLight'} />
		<Square xy="f1" color={'bg-squareDark'} />
		<Square xy="g1" color={'bg-squareLight'} />
		<Square xy="h1" color={'bg-squareDark'} />

		<Square xy="a2" color={'bg-squareDark'} />
		<Square xy="b2" color={'bg-squareLight'} />
		<Square xy="c2" color={'bg-squareDark'} />
		<Square xy="d2" color={'bg-squareLight'} />
		<Square xy="e2" color={'bg-squareDark'} />
		<Square xy="f2" color={'bg-squareLight'} />
		<Square xy="g2" color={'bg-squareDark'} />
		<Square xy="h2" color={'bg-squareLight'} />

		<Square xy="a3" color={'bg-squareLight'} />
		<Square xy="b3" color={'bg-squareDark'} />
		<Square xy="c3" color={'bg-squareLight'} />
		<Square xy="d3" color={'bg-squareDark'} />
		<Square xy="e3" color={'bg-squareLight'} />
		<Square xy="f3" color={'bg-squareDark'} />
		<Square xy="g3" color={'bg-squareLight'} />
		<Square xy="h3" color={'bg-squareDark'} />

		<Square xy="a4" color={'bg-squareDark'} />
		<Square xy="b4" color={'bg-squareLight'} />
		<Square xy="c4" color={'bg-squareDark'} />
		<Square xy="d4" color={'bg-squareLight'} />
		<Square xy="e4" color={'bg-squareDark'} />
		<Square xy="f4" color={'bg-squareLight'} />
		<Square xy="g4" color={'bg-squareDark'} />
		<Square xy="h4" color={'bg-squareLight'} />

		<Square xy="a5" color={'bg-squareLight'} />
		<Square xy="b5" color={'bg-squareDark'} />
		<Square xy="c5" color={'bg-squareLight'} />
		<Square xy="d5" color={'bg-squareDark'} />
		<Square xy="e5" color={'bg-squareLight'} />
		<Square xy="f5" color={'bg-squareDark'} />
		<Square xy="g5" color={'bg-squareLight'} />
		<Square xy="h5" color={'bg-squareDark'} />

		<Square xy="a6" color={'bg-squareDark'} />
		<Square xy="b6" color={'bg-squareLight'} />
		<Square xy="c6" color={'bg-squareDark'} />
		<Square xy="d6" color={'bg-squareLight'} />
		<Square xy="e6" color={'bg-squareDark'} />
		<Square xy="f6" color={'bg-squareLight'} />
		<Square xy="g6" color={'bg-squareDark'} />
		<Square xy="h6" color={'bg-squareLight'} />

		<Square xy="a7" color={'bg-squareLight'} />
		<Square xy="b7" color={'bg-squareDark'} />
		<Square xy="c7" color={'bg-squareLight'} />
		<Square xy="d7" color={'bg-squareDark'} />
		<Square xy="e7" color={'bg-squareLight'} />
		<Square xy="f7" color={'bg-squareDark'} />
		<Square xy="g7" color={'bg-squareLight'} />
		<Square xy="h7" color={'bg-squareDark'} />

		<Square xy="a8" color={'bg-squareDark'} />
		<Square xy="b8" color={'bg-squareLight'} />
		<Square xy="c8" color={'bg-squareDark'} />
		<Square xy="d8" color={'bg-squareLight'} />
		<Square xy="e8" color={'bg-squareDark'} />
		<Square xy="f8" color={'bg-squareLight'} />
		<Square xy="g8" color={'bg-squareDark'} />
		<Square xy="h8" color={'bg-squareLight'} /> -->
	</div>
	<!-- boardEnd -->

	<div class="size w-full flex file-bottom">
		<File text="a" />
		<File text="b" />
		<File text="c" />
		<File text="d" />
		<File text="e" />
		<File text="f" />
		<File text="g" />
		<File text="h" />
	</div>

	<div class="size h-full flex rank-right">
		<Rank rank={1} />
		<Rank rank={2} />
		<Rank rank={3} />
		<Rank rank={4} />
		<Rank rank={5} />
		<Rank rank={6} />
		<Rank rank={7} />
		<Rank rank={8} />
	</div>
</div>

<style>
	.gridLayout {
		container-type: inline-size;
		display: grid;
		grid-template-areas:
			'.. ft ft ft ft ft ft ft ft ..'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'rl b  b  b  b  b  b  b  b  rr'
			'.. fb fb fb fb fb fb fb fb ..';
	}

	.board {
		display: grid;
		grid-template-columns: repeat(8, 1fr);
		/* grid-template-rows: repeat(8, 1fr); */
		grid-area: b;
	}

	.file-top {
		grid-area: ft;
	}
	.file-bottom {
		grid-area: fb;
	}

	.rank-left {
		display: grid;
		grid-area: rl;
	}
	.rank-right {
		display: grid;
		grid-area: rr;
	}

	.size {
		font-size: 5cqw;
	}
</style>
