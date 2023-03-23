<script lang="ts">
	export let rank: 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8;
</script>

<span>{rank}</span>

<style>
	span {
		background-color: #38180b;
		color: white;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	span {
		flex-grow: 1;
		inline-size: 6cqw;
	}
</style>
