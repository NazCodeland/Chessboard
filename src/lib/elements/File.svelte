<script lang="ts">
	export let text: 'a' | 'b' | 'c' | 'd' | 'e' | 'f' | 'g' | 'h';
</script>

<span>{text}</span>

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
	}
</style>
