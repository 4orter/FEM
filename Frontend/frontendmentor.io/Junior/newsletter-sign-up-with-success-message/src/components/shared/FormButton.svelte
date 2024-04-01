<script>
	/** @type {string} */
	export let title;
</script>

<button type="submit">{title}</button>

<style>
	button {
		padding: 20px;
		margin-top: auto;
		border: none;
		border-radius: 10px;
		font-size: 1em;
		font-weight: bold;
		background-color: var(--navy-color);
		color: #ffffff;
		box-shadow: 0 0px 0px 0px rgba(255, 255, 255, 0);
		transition: box-shadow 150ms;
		cursor: pointer;
	}

	button:hover {
		background-color: var(--orange-color);
		box-shadow: 0 20px 30px 0px rgba(189, 75, 79, 0.5);
	}
</style>
