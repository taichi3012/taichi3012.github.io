<script lang="ts">
    import { fade } from "svelte/transition";
</script>

<svelte:head>
    <title>taichi3012's Portfolio</title>
</svelte:head>

<div class="article-container" in:fade>
    <h1>taichi3012's Portfolio</h1>
    <p>このポートフォリオは、私の概要や活動をまとめたものです。Firefox以外の主要なブラウザに対応しています。</p>
    <p>右上のボタンをクリックすることでライトテーマとダークテーマを切り替えることが出来ます。</p>
    <p>このWebサイトは<a href="https://kit.svelte.jp/" target="_blank" rel="noreferrer">SvelteKit</a>を使用して作成しました。</p>
        <h2>Link</h2>
        <ul>
            <!-- TODOリポジトリのURLを入れる -->
            <li><a href="https://github.com/taichi3012/taichi3012.github.io" target="_blank" rel="noreferrer">ソースコード</a></li>
        </ul>
</div>
