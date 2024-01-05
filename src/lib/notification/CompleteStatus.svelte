<script lang="ts">
	import PlayIcon from '$lib/icons/PlayIcon.svelte';

	export let name: string;
</script>

<div class="bridging-status flex gap-4 flex-col md:flex-row md:items-center">
	<div class="flex items-center gap-[18px] flex-1">
		<div
			class="min-w-16 min-h-16 flex justify-center items-center bg-black dark:bg-white rounded-lg text-[26px] dark:bg-opacity-10"
		>
			<PlayIcon />
		</div>

		<div class="flex flex-col flex-1 gap-1">
			<div class="text-large-bold">Your video is ready!</div>
			<p class="opacity-50 text-base">Watch the grand reveal video for your Cluster.</p>
		</div>
	</div>

	<a
		class="flex font-bold items-center justify-center gap-1.5 border border-neutral-300 p-[10px] rounded-lg whitespace-nowrap text-white bg-black dark:bg-white dark:text-black w-full md:w-fit text-base-bold"
		href="/share/{name}"
	>
		Watch video
	</a>
</div>
