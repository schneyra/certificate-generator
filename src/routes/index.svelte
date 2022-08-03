<script context="module">
	export const prerender = true;
</script>

<script>
	import Generator from '$lib/generator/Generator.svelte';

</script>

<svelte:head>
	<title>Certificate Generator</title>
	<meta name="description" content="Create your own certificates" />
</svelte:head>

<section>
	<h1>Certificate Generator</h1>

	<Generator></Generator>
</section>

<style>

</style>
