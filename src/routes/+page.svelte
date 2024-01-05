<script lang="ts">
	import { Notification } from '$lib/notification';

	let activeIndex = 0;

	const allStatus = ['bridging', 'video', 'complete'];
	$: activeStatus = allStatus[activeIndex];

	function onClick() {
		activeIndex = (activeIndex + 1) % allStatus.length;
	}
</script>

<div class="p-10 flex flex-col gap-10">
	<Notification status={activeStatus} name="ryeshrimp" address="0x0000" />

	<button class="bg-neutral-200 px-6 py-2" on:click={onClick}>Change status</button>
</div>
