<script lang="ts">
    import { page } from "$app/stores";
    import { fade } from "svelte/transition";
</script>

{#key $page.url.pathname}
    <div class="article-container" in:fade>
        <slot />
    </div>
{/key}
