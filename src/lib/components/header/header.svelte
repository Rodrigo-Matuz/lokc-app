<script lang="ts">/** biome-ignore-all lint/correctness/noUnusedImports: They are being used */
/** biome-ignore-all lint/style/useConst: must be let */

    import { Settings } from "@lucide/svelte";
    import { Button } from "$components/ui/button";
    import { Input } from "$components/ui/input";

    
    export let headerIcon = Settings
    export let inputDisable = true;
    export let inputPlaceholder = "";

</script>

<div class="flex gap-5 bg-background m-5">
    <Input 
        class="shadow-none bg-border focus-visible:bg-border focus-visible:border-x-0 focus-visible:border-t-0 focus-visible:border-b-2 focus-visible:border-b-secondary outline-none focus-visible:ring-0 h-11 text-1xl! text-center caret-secondary disabled:cursor-not-allowed rounded!"
        type="text"
        placeholder={inputPlaceholder}
        disabled={inputDisable}
    />
    <Button class="w-12 h-11 rounded!" size="lg">
        <svelte:component this={headerIcon}  class="size-8"/>
    </Button>
</div>