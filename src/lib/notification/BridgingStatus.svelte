<script lang="ts">
	import ExternalIcon from '$lib/icons/ExternalIcon.svelte';

	export let name: string;
</script>

<div class="bridging-status flex flex-col gap-4 md:flex-row md:items-center">
	<div class="flex items-center gap-[18px] flex-1">
		<div
			class="min-w-16 min-h-16 flex justify-center items-center bg-neutral-200 dark:bg-neutral-700 rounded-full"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="36"
				height="36"
				viewBox="0 0 36 36"
				fill="none"
			>
				<path
					opacity="0.3"
					d="M18 1.5C14.7366 1.5 11.5465 2.46771 8.8331 4.28075C6.11969 6.09379 4.00484 8.67074 2.756 11.6857C1.50715 14.7007 1.18039 18.0183 1.81705 21.219C2.45371 24.4197 4.02518 27.3597 6.33275 29.6673C8.64031 31.9748 11.5803 33.5463 14.781 34.183C17.9817 34.8196 21.2993 34.4929 24.3143 33.244C27.3293 31.9952 29.9062 29.8803 31.7193 27.1669C33.5323 24.4535 34.5 21.2634 34.5 18C34.5 13.6239 32.7616 9.42709 29.6673 6.33274C26.5729 3.23839 22.3761 1.5 18 1.5ZM18 30C15.6266 30 13.3066 29.2962 11.3332 27.9776C9.35977 26.6591 7.8217 24.7849 6.91345 22.5922C6.0052 20.3995 5.76756 17.9867 6.23058 15.6589C6.69361 13.3311 7.8365 11.1929 9.51473 9.51472C11.193 7.83649 13.3312 6.6936 15.6589 6.23058C17.9867 5.76755 20.3995 6.00519 22.5922 6.91345C24.7849 7.8217 26.6591 9.35977 27.9776 11.3332C29.2962 13.3065 30 15.6266 30 18C30 21.1826 28.7357 24.2348 26.4853 26.4853C24.2349 28.7357 21.1826 30 18 30Z"
					fill="#3B82F6"
				/>
				<path
					d="M15.2098 1.74C11.8546 2.30606 8.75643 3.89558 6.33968 6.29085C3.92294 8.68611 2.30582 11.77 1.70982 15.12C1.63824 15.4401 1.63346 15.7715 1.69578 16.0936C1.7581 16.4156 1.88618 16.7213 2.072 16.9916C2.25783 17.2619 2.49742 17.491 2.77578 17.6645C3.05415 17.838 3.36531 17.9522 3.68982 18C4.27405 18.056 4.85736 17.8845 5.31836 17.5213C5.77937 17.1581 6.08255 16.6311 6.16482 16.05C6.57369 13.5558 7.75962 11.2545 9.55352 9.47404C11.3474 7.69362 13.6577 6.52506 16.1548 6.135C16.6639 6.06628 17.131 5.8159 17.47 5.43C17.809 5.0441 17.9972 4.54868 17.9998 4.035C17.997 3.69053 17.9186 3.35087 17.7702 3.03999C17.6218 2.72911 17.407 2.45456 17.141 2.23572C16.8749 2.01688 16.5641 1.85907 16.2304 1.77342C15.8968 1.68777 15.5484 1.67636 15.2098 1.74Z"
					fill="#3B82F6"
				>
					<animateTransform
						attributeName="transform"
						type="rotate"
						from="0 18 18"
						to="360 18 18"
						dur=".3s"
						repeatCount="indefinite"
					/>
				</path>
			</svg>
		</div>

		<div class="flex flex-col flex-1 gap-1">
			<div class="text-large-bold">Creating your cluster</div>
			<p class="text-base">
				<span class="opacity-50">Your cluster, </span><span class="opacity-100 text-base"
					>{name}/</span
				><span class="opacity-50">, will be ready soon.</span>
			</p>
		</div>
	</div>

	<a
		class="flex items-center justify-center gap-1.5 border border-neutral-300 dark:border-neutral-600 p-[10px] rounded-lg dark:bg-neutral-700 w-full md:w-fit text-base-bold"
		href="/"
		target="_blank"
	>
		<span>Transaction</span>
		<span class="text-xl opacity-50"><ExternalIcon /></span>
	</a>
</div>
