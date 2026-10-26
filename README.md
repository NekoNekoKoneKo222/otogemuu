# PULSE REQUIEM（音ゲー × 弾幕シューティング）

ブラウザで動作するオリジナルのリズム・ボスバトルゲーム。追加ライブラリなし、`dist/index.html` 単体でプレイできます。

## 操作

| 入力 | 動作 |
|---|---|
| W / A / S / D | 移動 |
| マウス移動 | 狙う方向 |
| 左クリック | 近距離の剣攻撃 |
| **Space** | **弓の遠距離攻撃** |
| Shift | 回避ダッシュ（短時間無敵、クールダウンあり） |
| P | 第一形態のみ一時停止／再開 |

右クリックも遠距離攻撃の補助操作として利用可能です。ブラウザのコンテキストメニューはゲーム画面内では無効化しています。

## リズムシステム

- 130 BPM のオリジナルシンセBGMを Web Audio API で生成。
- 拍に合わせて剣や弓を使うと PERFECT / GREAT / GOOD の判定が出ます。
- 高精度で威力・スコア・コンボ・RESONANCEが増えます。
- 同じ拍での連打は重複してコンボにならず、OFF BEAT扱いです。

## ボスと第二形態

- ボスは音楽の拍に合わせて弾幕を発射します。
- HPが約52%以下になると第二形態に移行し、弾幕が大幅に強化されます。
- **第二形態から一時停止が封印**されます。Pを押すと PAUSE DENIED の警告が出ますが、戦闘は継続します。
- 画面外や別ウィンドウへ移動した際の自動ポーズも、第一形態にのみ適用します。
- HP0で敗北、制限時間内にボスHP0で勝利します。

## Render Static Site

- Repository: `https://github.com/NekoNekoKoneKo222/otogemuu`
- Branch: `main`
- Build Command: `echo "Static game ready"`
- Publish Directory: `dist`
- Auto Deploy: `Yes`

ユーザーアカウントやデータベースは不要です。ハイスコアのみブラウザの localStorage に保存します。
