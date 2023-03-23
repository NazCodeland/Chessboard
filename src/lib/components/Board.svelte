<script lang="ts">
	import Square from '$lib/elements/Square.svelte';
	import QueenLight from '$lib/SVGs/QueenLight.svelte';
	import QueenDark from '$lib/SVGs/QueenDark.svelte';
	import File from '$lib/elements/File.svelte';
	import Rank from '$lib/elements/Rank.svelte';
	export let size: unknown;
</script>

<div class="gridLayout place-items-center">
	<div class="h-full flex rank-left">
		<Rank rank={1} />
		<Rank rank={2} />
		<Rank rank={3} />
		<Rank rank={4} />
		<Rank rank={5} />
		<Rank rank={6} />
		<Rank rank={7} />
		<Rank rank={8} />
	</div>

	<div class="test flex w-full file-top">
		<File text="a" />
		<File text="b" />
		<File text="c" />
		<File text="d" />
		<File text="e" />
		<File text="f" />
		<File text="g" />
		<File text="h" />
	</div>

	<!-- board -->
	<div style="inline-size:{size}; block-size:{size}" class="board">
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
	</div>
	<!-- boardEnd -->

	<div class="w-full flex file-bottom">
		<File text="a" />
		<File text="b" />
		<File text="c" />
		<File text="d" />
		<File text="e" />
		<File text="f" />
		<File text="g" />
		<File text="h" />
	</div>

	<div class="h-full flex rank-right">
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
		container-type: size;
		font-size: 1cqw;
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
		/* container-type: size; */
		display: grid;
		grid-area: b;
		grid-template-columns: repeat(8, 1fr);
		/* grid-template-rows: repeat(8, 1fr); */
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

	.test {
		font-size: inherit;
	}
</style>
