<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="container">
	{@render children()}
</div>

<style>
	.container {
    max-width: 800px;
    margin-inline: auto;
    margin-top: min(64px, 5 vh);
  }
</style>