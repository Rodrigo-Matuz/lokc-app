<script lang="ts">
	// biome-ignore lint/style/useImportType: 'ProgressPrimitive' cannot be used as a value because it was imported using 'import type'.
	import  { Progress as ProgressPrimitive } from "bits-ui";
	import { cn, type WithoutChildrenOrChild } from "$utils/index";

	// biome-ignore lint/style/useConst: Must use let due to problem at: bind:this={ref}
	let {
		ref = $bindable(null),
		class: className,
		max = 100,
		value,
		...restProps
	}: WithoutChildrenOrChild<ProgressPrimitive.RootProps> = $props();
</script>

<ProgressPrimitive.Root
	bind:ref
	data-slot="progress"
	class={cn("relative bg-primary/20 rounded-full w-full h-2 overflow-hidden", className)}
	{value}
	{max}
	{...restProps}
>
	<div
		data-slot="progress-indicator"
		class="flex-1 bg-primary w-full h-full transition-all"
		style="transform: translateX(-{100 - (100 * (value ?? 0)) / (max ?? 1)}%)"
	></div>
</ProgressPrimitive.Root>
