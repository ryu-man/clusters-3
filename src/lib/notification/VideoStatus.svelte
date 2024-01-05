<script lang="ts">
	import Progress from '$lib/Progress.svelte';

	export let name: string;
</script>

<div class="bridging-status flex gap-4 flex-col md:flex-row md:items-center">
	<div class="flex items-center gap-[18px] flex-1">
		<Progress value={0.89} />

		<div class="flex flex-col flex-1 gap-1">
			<div class="text-large-bold">Your cluster is ready!</div>
			<p class="opacity-50 text-base">
				We are still working on your reveal video. Set up your cluster in the meantime.
			</p>
		</div>
	</div>

	<a
		class="flex font-bold items-center justify-center gap-1.5 p-[10px] rounded-lg whitespace-nowrap bg-[#627EEA] text-white w-full md:w-fit text-base-bold"
		href="/profile/{name}"
	>
		View cluster
	</a>
</div>
