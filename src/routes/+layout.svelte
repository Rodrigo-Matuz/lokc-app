<script lang="ts">
    import "./layout.css"
    // biome-ignore lint/correctness/noUnusedImports: Is is being used
    import { ModeWatcher } from "mode-watcher";

    // biome-ignore lint/correctness/noUnusedVariables: For now it's there following standarts for tailwind css
    // biome-ignore lint/style/useConst: <explanation>
    let { children } = $props();
</script>

<ModeWatcher defaultMode="dark" />

{@render children?.()}