<script lang="ts">
    import { onMount } from "svelte";


    let darkTheme: boolean;

    function toggleTheme() {
        darkTheme = !darkTheme;

        if (darkTheme) {
            localStorage.setItem('theme', 'dark');
            document.documentElement.setAttribute('theme', 'dark');
        } else {
            localStorage.removeItem('theme');
            document.documentElement.removeAttribute('theme');
        }
    }

    onMount(() => {
        darkTheme = localStorage.getItem('theme') === 'dark';
        if (darkTheme) {
            document.documentElement.setAttribute('theme', 'dark');
        }
    });
</script>

<button type="button" on:click={toggleTheme}>
    <div class="vbox{darkTheme ? ' dark-mode': ''}">
        <span class="material-icons light-mode-icon">light_mode</span>
        <span class="material-icons dark-mode-icon">dark_mode</span>
    </div>
</button>

<style>
    button {
        height: 24px;
        width: 48px;
        padding: 0;
        overflow: hidden;
        background: none;
        border: none;
        cursor: pointer;
        user-select: none;
    }

    div {
        transition: transform 1s;
    }

    .dark-mode {
        transform: rotate(180deg);
    }

    .light-mode-icon {
        color: #000000;
    }

    .dark-mode-icon {
        color: #FFFFFF;
        transform: rotate(180deg);
    }
</style>
