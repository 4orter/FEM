<script>
	/** @type {number} */
	export let maxWidth = 1000;
</script>

<div style={`max-width: ${maxWidth}px;`}>
	<slot />
</div>

<style >
	div {
		background: #fff;
		border-radius: 40px;
		padding: 20px;
		margin: 0 auto;
		box-shadow: 5px 10px 20px 20px rgba(0, 0, 0, 0.4);
	}

	@media (max-width: 500px) {
		div {
			padding: 0;
			border-radius: 0;
			width: 100%;
		}
	}
</style>
