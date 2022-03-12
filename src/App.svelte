<script>
	import PeopleTable from "./Table/PeopleTable.svelte";

	function reload() {
		window.location.reload()
	}
</script>

<main>
	<h1>Here's some people out there...</h1>
	<PeopleTable />
	<button on:click="{reload}">
		See others
	</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 100;
	}

	button {
		color: #ff3e00;
		border-color: #ff3e00;
		background-color: white;
		font-size: 1em;
	}

	button:hover {
		color: white;
		background-color: #ff3e00;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>