<script lang="ts">
    import "../layout.css";
    // biome-ignore lint/correctness/noUnusedImports: Is is being used
    import { ModeWatcher } from "mode-watcher";

    // biome-ignore lint/correctness/noUnusedVariables: For now it's there following standarts for tailwind css
    const { children } = $props();
</script>

<ModeWatcher defaultMode="dark" />

{@render children?.()}