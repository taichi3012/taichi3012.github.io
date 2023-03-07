<script lang="ts">
    import { page } from '$app/stores';
    import ThemeButton from './ThemeButton.svelte';
    import './app.css';
</script>

<header>
    <label class="menu-toggle material-icons">
        <input type="checkbox">
    </label>
    <nav>
        <ul>
            <li>
                <a
                    href="/"
                    aria-current={$page.url.pathname === "/" ? "page" : undefined}
                >
                    Home
                </a>
            </li>
            <li>
                <a
                    href="/about"
                    aria-current={$page.url.pathname === "/about" ? "page" : undefined}
                >
                    About
                </a>
            </li>
            <li>
                <a
                    href="/products"
                    aria-current={$page.url.pathname === "/products" ? "page" : undefined}
                >
                    Products
                </a>
            </li>
            <li>
                <a
                    href="/skill"
                    aria-current={$page.url.pathname === "/skill" ? "page" : undefined}
                >
                    Skill
                </a>
            </li>
        </ul>
    </nav>
    <div class="theme-button">
        <ThemeButton />
    </div>
</header>

<main>
    <slot />
</main>

<style>
    header {
        position: sticky;
        top: 0;
        left: 0;
        z-index: 1;
        display: flex;
        justify-content: center;
        width: 100%;
        height: 3em;
        background-color: var(--foreground);
        transition: background-color 2s;
    }

    ul {
        display: flex;
        margin: 0;
        padding: 0;
        list-style: none;
    }

    li {
        margin: 0.5em;
    }

    a {
        font-size: 1.5em;
        color: var(--text-sub);
        text-decoration-line: none;
        transition: none;
    }

    a[aria-current="page"] {
        color: var(--text-main);
    }

    .theme-button {
        position: absolute;
        right: 0.5em;
        align-self: center;
    }

    .menu-toggle {
        display: none;
    }

    .menu-toggle > input[type="checkbox"] {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        margin: 0;
        appearance: none;
        -webkit-appearance: none;
    }

    @media screen and (max-width: 768px) {
        .menu-toggle {
            display: block;
            position: absolute;
            left: 0.5em;
            align-self: center;
        }

        .menu-toggle::before {
            content: "menu";
        }

        .menu-toggle:has(input[type="checkbox"]:checked)::before {
            content: "close";
        }

        nav {
            display: none;
        }

        .menu-toggle:has(input[type="checkbox"]:checked) + nav {
            display: block;
            position: absolute;
            left: 0;
            top: 100%;
            width: 100%;
            background-color: var(--foreground);
            transition: background-color 2s, height 2s;
        }

        .menu-toggle:has(input[type="checkbox"]:checked) + nav > ul {
            display: flex;
            flex-direction: column;
            margin-left: 1em;
        }
    }
</style>
