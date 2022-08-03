<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	&copy; <a href="https://martinschneider.me">Martin Schneider</a>
</footer>

<style>
	footer {
		background: lightsteelblue;
	}
</style>
