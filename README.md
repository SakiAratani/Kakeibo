# 家計簿アプリ（支出・予算専用版）　iPhoneへの入れ方

## 中身
- index.html … アプリ本体
- sw.js … オフラインで起動するための仕組み
- manifest.json / icon-180.png / icon-512.png … ホーム画面用の名前とアイコン

## 前の版をすでに公開している場合
GitHubのリポジトリで「Add file → Upload files」から5つのファイルをすべてアップロードし直します（同じ名前のファイルは上書きされます）。
iPhoneでアプリを一度開き直すと新しい版に切り替わります。切り替わらないときは、アプリを完全に閉じてから2回ほど開き直してください。
前の版で記録した支出は自動で引き継がれます（収入は取り込まれません）。

## 初めて公開する場合（GitHub Pages・無料）
1. github.com で「New repository」を作る（例：kakeibo、Public）。
2. 「Add file → Upload files」で5つのファイルをアップロードし「Commit changes」。
3. 「Settings → Pages」で Branch を「main」「/(root)」にして保存。
4. 1〜2分後に表示される https://ユーザー名.github.io/kakeibo/ をSafariで開く。
5. 共有ボタン →「ホーム画面に追加」。

※記録したデータはiPhone内にだけ保存され、GitHubには送られません。

## バックアップ
設定 →「バックアップを書き出す（JSON）」→「"ファイル"に保存」。月1回程度がおすすめです。
前の版のバックアップファイルも読み込めます（支出だけが取り込まれます）。

## 今後アプリを更新するとき
index.html を差し替えたら、sw.js の `kakeibo-v4` を `kakeibo-v5` のように変えてアップロードしてください。
