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
		text-align: center;
	}
	span {
		inline-size: 80px;
	}
</style>
