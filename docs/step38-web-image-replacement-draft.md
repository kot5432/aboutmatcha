# STEP 38｜P5をWebデモ実画像に統一（Canva保存前プレビュー）

更新日：2026-11-12
状態：**Canva上にv14 PPTXを複製インポートし、5枚目の3画像をWebデモの同じ画像へ差し替えた編集ドラフトを用意。Canva側の指示に従い、プレビュー確認・利用者承認前は保存コミットしない。PPTX/PDF v14はまだ変更していない。**

## ユーザーの判断
- P5の3商品はWebデモのまま維持し、新しく生成した画像ではなく、**Webデモ内で実際に使用しているイラスト**を使う。
- 商品：抹茶バスクチーズ、抹茶ブリュレクレープ、生茶の菓アイスバー。

## 元画像
以下の3つを `kot5432/matcha` のGitHub `assets` から参照し、Canvaのメディアとしてアップロード（画像の再生成なし）。

1. https://raw.githubusercontent.com/kot5432/matcha/main/assets/matcha-basque-cheesecake.jpg
2. https://raw.githubusercontent.com/kot5432/matcha/main/assets/matcha-brulee-crepe.jpg
3. https://raw.githubusercontent.com/kot5432/matcha/main/assets/matcha-ice-bar.jpg

## ドラフト編集
- v14 PPTXをCanvaに取り込み、9ページの編集デザインを生成（ID `DAHarNLLDJU`）。
- **5ページ目の画像要素3点だけ**を上記3画像に置換。商品名・説明・商品順・レイアウト・他ページは変更対象外。
- 3件のCanva画像アセットID（配置確認用）：`MAHarMGTXHs`、`MAHarADQjmc`、`MAHarECTPRM`。
- 編集トランザクション `3721621099694636134` で更新処理が成功。変更後のfill参照も再確認。
- Canvaプレビューが返されたが、ホスト側の画像ダウンロード制限によりローカル画像としては取得できていない。Canvaのドラフトビューで確認を依頼する。
- Canvaドラフト編集リンク（ユーザーがアクセスできる場合）：https://www.canva.com/d/AIPNDoUeRMeaqol
- Canva元デザイン： https://www.canva.com/d/cmcj3KmpZt_nu4O

## 未完了事項
- 5ページ目のプレビューを本人が確認し、保存する明示承認を得る。
- Canvaで最終保存を実施、必要ならCanvaからPDF/PPTXにエクスポート。
- もしCanva由来の再書き出しでv14の他ページにレイアウトやリンクの差分が出たら、改めてPDF/PPTXを検査し、v15完成とする。
- **元のv14 PDF/PPTXを完成v15と呼び替えたり、未確認の差し替えが済んだと宣言したりしない。**

## 注意
- 画像はWebに採用中の「イメージイラスト」であり、権利を取得した公式商品写真だとは扱わない。
- GitHubに個人写真や応募PDF/PPTXのバイナリを無断アップロードしない。

## 追記｜ユーザーの明示指示に基づくCanva保存完了（2026-11-12）

ユーザーから「Webの画像そのものを使う」「そうです」「取れないですか？画像など」と繰り返し指定を受けたため、Canva編集トランザクション `3721621099694636134` をコミット。ツール応答は `status: committed`。編集用デザインの3画像は、GitHub `kot5432/matcha` の公開アセットと同一の3ファイルをCanvaへ取り込んで配置した。

- 保存済みCanvaデザイン：https://www.canva.com/d/cmcj3KmpZt_nu4O
- デザインID：`DAHarNLLDJU`
- 変更対象：5ページ目の画像3点のみ
- 画像ソース：`assets/matcha-basque-cheesecake.jpg`、`assets/matcha-brulee-crepe.jpg`、`assets/matcha-ice-bar.jpg`
- Canva側のアセット差し替えと保存成功を確認したが、**新しいPDF／PPTXファイルのエクスポートは未実行・未検査**。v14のローカルPDF／PPTXは変更していない。Canva保存済みデザインが最新版。

## 2026-11-12｜PDF・PPTXの書き出しについて

ユーザーからWebと同じ画像3件への差し替え確定と出力の許可を受領。Canvaデザイン `DAHarNLLDJU` には差し替えが保存済み。

ただし、現在のツール経路ではCanvaからローカルPDF・PPTXの直接エクスポートができず、他サービスへのインポート経路も利用不可。GitHubからバイナリの元画像を直接ローカルファイルへ転送することもできなかった。そのため、**v15 PDF・PPTXは未作成**。v14のPDF・PPTXをv15として再配布しない。

**最新の正しい画像が反映された成果物はCanva上の9ページデザインのみ**：https://www.canva.com/d/cmcj3KmpZt_nu4O 。ユーザーがCanva上でPDF・PowerPointとしてエクスポート可能。エクスポート後のファイルのリンクや内部ハイパーリンク、全ページの表示確認は未実施。
