<script lang="ts">
	type Status = 'bridging' | 'video' | 'complete';
	export let status: Status;
	export let name: string;
	export let address: string;
</script>

<div
	class="notification font-medium bg-neutral-100 dark:bg-neutral-800 text-neutral-900 dark:text-white pl-5 py-4 pr-7 border border-neutral-300 dark:border-neutral-600 rounded-[14px]"
>
	{#if status === 'bridging'}
		<!-- Bridging status -->
		{#await import('./BridgingStatus.svelte') then Status}
			<Status.default {name} />
		{/await}
	{:else if status === 'video'}
		<!-- Video status -->
		{#await import('./VideoStatus.svelte') then Status}
			<Status.default {name} />
		{/await}
	{:else}
		<!-- Complete status -->
		{#await import('./CompleteStatus.svelte') then Status}
			<Status.default {name} />
		{/await}
	{/if}
</div>

<style lang="postcss">
	@media (prefers-color-scheme: dark) {
		.notification {
			box-shadow: 0px 4px 164px 0px rgba(255, 255, 255, 0.25);
		}
	}
</style>
