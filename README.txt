KEEPSAFE DataGuard アプリ版(PWA)公開手順
==================================
このフォルダ一式を「HTTPSで公開できる静的ホスティング」に置くと、ホーム画面やアプリとしてインストールできます。
(ファイルを直接開く file:// や、claude.ai の共有ページでは、アプリとしてインストールできません。)

■ いちばん簡単:Netlify Drop
 1. https://app.netlify.com/drop を開く
 2. この pwa フォルダをそのままドラッグ&ドロップ
 3. 発行されたURL(https://〜.netlify.app)を、スマホやパソコンで開く

■ GitHub Pages
 1. リポジトリを作り、pwa フォルダの中身(index.html など)をルートに置く
 2. Settings → Pages → Branch: main / (root) を選んで保存
 3. https://ユーザー名.github.io/リポジトリ名/ を開く

■ Cloudflare Pages / Vercel など
 静的サイトとして、このフォルダをそのまま公開すればOKです。

■ インストール
 iPhone: Safari → 共有 → ホーム画面に追加
 Android: Chrome → メニュー → アプリをインストール
 PC: Chrome/Edge のアドレスバー右のインストールボタン

■ 更新するとき
 index.html を差し替え、sw.js の先頭 V='keepsafe-v1' の数字を上げて再公開してください。

■ 注意
 ・保管庫の中身は、公開URLごと・端末ごとに別です。claude.ai の共有ページで作った保管庫は引き継がれません(「機種変更:メールで送る」で移せます)。
 ・公開URLを知っている人は誰でもページを開けます。保管庫の中身はあなたの端末内にあり、サーバーには送られません。
