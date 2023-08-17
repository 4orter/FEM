<script>
	/** @type {string} */
	export let label;
	/** @type {'text' | 'email' | 'password'} */
	export let type;
	/** @type {string} */
	export let name;
	/** @type {string} */
	export let placeholder = '';
	/** @type {string} */
	export let errorMessage = '';
	/** @type {string} */
	export let defaultValue = '';
</script>

<label class="{errorMessage ? 'inputError' : null}">
	<span>{label}</span>
	<input
		type={type}
		name={name}
		placeholder={placeholder ?? null}
		value={defaultValue}
		on:input={() => errorMessage = ''}
	/>
	{#if errorMessage}
		<small>{errorMessage}</small>
	{/if}
</label>

<style>
	label {
		display: flex;
		flex-direction: column;
		padding-top: 20px;
	}

	label > span {
		font-weight: bold;
		margin-bottom: 10px;
	}

	input {
		padding: 20px;
		border: 2px solid var(--inactive-color);
		border-radius: 8px;
		font-size: 1.1em;
	}

	input::placeholder {
		opacity: 1;
		color: var(--inactive-color);
	}

	input:focus {
		outline: none;
		border: 2px solid var(--orange-color);
	}

	label.inputError > span {
		color: red;
	}

	label.inputError > input {
		border-color: red;
		background-color: rgba(255, 0, 0, 0.1);
	}

	label.inputError > small {
		margin-top: 8px;
		color: red;
	}
</style>
