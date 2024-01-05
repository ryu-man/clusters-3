<script lang="ts">
	import Progress from '$lib/Progress.svelte';

	export let name: string;
</script>

<div class="bridging-status flex items-center gap-[18px]">
	<Progress value={0.89} />

	<div class="flex flex-col flex-1 gap-1">
		<div class="text-large-bold">Your cluster is ready!</div>
		<p class="opacity-50 text-base">
			We are still working on your reveal video. Set up your cluster in the meantime.
		</p>
	</div>

	<a
		class="flex font-bold items-center gap-1.5 px-4 py-3 rounded-lg whitespace-nowrap bg-[#627EEA] text-white"
		href="/profile/{name}"
	>
		View cluster
	</a>
</div>
