<script>
    import IllustrationMobile from "./IllustrationMobile.svelte";
</script>

<div class="spotlight">
	<IllustrationMobile />
</div>

<style>
	div {
		display: none;
		width: 100%;
		align-items: center;
		justify-content: center;
	}

	@media (max-width: 900px) {
		div {
			width: 100%;
			display: flex;
		}
	}
</style>
