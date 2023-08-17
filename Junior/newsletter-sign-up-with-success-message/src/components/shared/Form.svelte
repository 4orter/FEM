<script>
	import ListItem from "./ListItem.svelte";
	import FormInput from "./FormInput.svelte";
	import FormButton from "./FormButton.svelte";

	/** @type {string} */
	export let formError;
	/** @type {string} */
	export let defaultValue = '';

	const items = [
		"Product discovery and building what matters",
		"Measuring to ensure updates are a success",
		"And much more!"
	];
</script>

<article>
	<h1>Stay updated!</h1>
	<p>Join 60,000+ product managers receiving monthly updates on:</p>
	<ul>
		{#each items as item}
			<ListItem content={item} />
		{/each}
	</ul>
	<form id="form" method="post" action="/">
		{#if formError}
			<FormInput
				type="email"
				label="Email address"
				placeholder="email@company.com"
				name="email"
				errorMessage={formError}
				defaultValue={defaultValue}
			/>
		{:else}
			<FormInput
				type="email"
				label="Email address"
				placeholder="email@company.com"
				name="email"
			/>
		{/if}
		<FormButton title="Subscribe to Monthly Newsletter" />
	</form>
</article>

<style>
	article {
		padding: 60px;
	}

	article > * {
		margin-bottom: 20px;
	}

	h1 {
		font-size: 3.5em;
	}

	form {
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		gap: 15px;
	}

	@media (max-width: 900px) {
		article {
			padding: 25px;
		}

		h1 {
			font-size: 2.5em;
		}
	}
</style>
