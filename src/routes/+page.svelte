<script>
	import MemoryLeak from './MemoryLeak.svelte';

	let counter = $state(0);
</script>

<button onclick={() => (counter += 1)}>Toggle</button>
{#if counter % 2 === 1}
	<MemoryLeak />
{/if}
