<script>
</script>

<svelte:head>
	<title>Basics</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<table>
		<tr>
			<th>Data</th>
			<th>Value</th>
		</tr>
		<tr>
			<td>Roll</td>
			<td>10</td>
		</tr>
	</table>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	table {
		border-width: 1;
		border-color: black;
	}
</style>
