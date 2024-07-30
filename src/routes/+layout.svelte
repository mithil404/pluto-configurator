<script>
	import Header from './Header.svelte';
	import Tabs from './Tabs.svelte';
	import '../app.css';
</script>

<div class="app">
	<Header />
	<div class="body">
		<Tabs />
		<main>
			<slot />
		</main>
	</div>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	.body {
		display: flex;
		flex-grow: 1;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>
