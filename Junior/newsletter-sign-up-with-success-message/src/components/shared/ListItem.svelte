<script>
	import ListIcon from "./ListIcon.svelte";

	/** @type {string} */
	export let content;
</script>

<li>
	<span>
		<ListIcon />
	</span>
	<span>{content}</span>
</li>

<style>
	li {
		display: flex;
		gap: 20px;
	}
</style>
