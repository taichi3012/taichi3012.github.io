<svelte:head>
    <title>Products</title>
</svelte:head>

<h1>PRODUCTS</h1>
    <h2>Thelowダメージ計算機</h2>
    <p>
        Java版Minecraftで遊べる、<a href="https://portal.eximradar.jp/thelow/" target="_blank" rel="noreferrer">TheLow</a>というRPGサーバーの武器の攻撃力を計算出来る非公式のWebサイトです。
    </p>
    <p>
        計算の内容を、URLパラメーターや動的OGP画像などで共有できる機能があるのが特徴です。
    </p>
    <p>
        例えば、<a href="https://tldc.vercel.app/?wd=jU&ns=1&ms=11" target="_blank" rel="noreferrer">https://tldc.vercel.app/?wd=jU&ns=1&ms=11</a>というURLをTwitterなどのSNSに貼り付けると以下のようなOGP画像が表示されます。
    </p>
    <a href="https://tldc.vercel.app/api/og.png/?wd=jU&ns=1&ms=11" target="_blank" rel="noreferrer">
        <img src="https://tldc.vercel.app/api/og.png?wd=jU&ns=1&ms=11" alt="動的OGP画像の例">
    </a>
    <p>
        OGP画像の動的生成にはVercel社製の<a href="https://www.npmjs.com/package/satori" target="_blank" rel="noreferrer">satori</a>というパッケージを利用しました。また、HTMLとCSSをsatoriが対応しているReactNodeに変換するために、<a href="https://www.npmjs.com/package/satori-html" target="_blank" rel="noreferrer">satori-html</a>というパッケージも利用しました。
    </p>
    <p>
        開発面でのことなのですが、HTML,CSS,JavaScriptを初めて使用したため、一番最初の段階ではレイアウトや装飾などがまったく出来ていないものでした。ですが、コントリビュートをしてくださった方がいて、見栄えの改善や機能の追加、フレームワークへの移行などをしてくださいました。
    </p>
    <p>
        このことがWeb系の技術に関する興味を持つきっかけになり、同時に知識を深めるきっかけにもなりました。とても感謝しています。
    </p>
        <h3>Link</h3>
        <ul>
            <li><a href="https://taichi3012.github.io/ThelowDamageCalculation" target="_blank" rel="noreferrer">GitHubPages版</a></li>
            <li><a href="https://tldc.vercel.app/" target="_blank" rel="noreferrer">Vercel版</a></li>
            <li><a href="https://github.com/taichi3012/ThelowDamageCalculation" target="_blank" rel="noreferrer">リポジトリ</a></li>
        </ul>

    <h2>TheLowTooltipMod</h2>
    <p>
        こちらもRPGサーバーのTheLowで使用できるもので、Minecraftの改造クライアントのForgeで利用できるModです。
    </p>
    <p>
        持っている武器の攻撃力を攻撃する敵の種類ごとに計算したり、ゲーム内の攻撃手段である「武器スキル」の<abbr title="発動できる間隔">クールタイム</abbr>を計算することが出来ます。
    </p>
    <p>
        TheLowには攻撃力や武器スキルのクールタイムを増減させる様々な要素があり、それを武器ごとに計算するのが大変だと感じたため製作しました。
    </p>
        <h3>Link</h3>
        <ul>
            <li><a href="https://github.com/taichi3012/TheLowTooltipMod" target="_blank" rel="noreferrer">リポジトリ</a></li>
        </ul>

<style>
    img {
        max-width: 80%;
    }
</style>
