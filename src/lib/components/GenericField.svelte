<script>
	import InfoPopover from './InfoPopover.svelte';
	export let title;
	export let infoPopOverText = null;
	export let value;
	export let textHeight = 'text-lg md:text-nowrap';
	export let cols = 1;
</script>

<div class="flex flex-col col-span-{cols} gap-1 align-text-bottom">
	{#if infoPopOverText != null}
		<span class="inline-flex font-bold md:whitespace-nowrap"
			>{title} <InfoPopover text={infoPopOverText} /></span
		>
	{:else}
		<span class="inline-flex font-bold">{title}</span>
	{/if}
	<div class="inline-flex md:whitespace-nowrap">
		<span class={textHeight}>{value}</span>
	</div>
</div>
