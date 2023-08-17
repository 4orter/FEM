<script>
    import IllustrationDesktop from "./IllustrationDesktop.svelte";
</script>

<div class="spotlight">
	<IllustrationDesktop />
</div>

<style>
	div {
		width: 50%;
		display: flex;
		align-items: center;
		justify-content: flex-end;
	}

	@media (max-width: 900px) {
		div {
			display: none;
		}
	}
</style>
