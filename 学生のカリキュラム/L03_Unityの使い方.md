# Unityの使い方

<div style="text-align: right;">
2019年11月11日<br>
株式会社アルファオメガ  松本清明
</div>


## シーン遷移
  ・タイトルー＞メイン画面ー＞オプション画面

## Canvas

## BigButton

## スクリーンフェード

## TextMeshProでタイトル名を表示

## TextMesh ProでDynamic SDF Systemで文字を出す。

1. `Window>TextMeshPro>FontAssetCreator`で`FontFontAsset`を作成
1. FontAssetを選択
1. Generation Settingsの項目を埋める
```
   Source Font Fileに、フォントファイル（otf等）を指定
   Atlas Population ModelをDynamicに変更
   Atlas Render ModeはSDF AA
  Sample Point Sizeは60前後にしておく
  （文字の解像度に依存、大きいとフォントがすぐ一杯になる）
  Atlas Wideth、Atlas Heightは少し大きめにする
  （文字を表示出来る量に依存、小さいとすぐ一杯になる）
```
1. Applyを押す

http://tsubakit1.hateblo.jp/entry/2019/02/02/060758


  使い方の手順を書く
　日本語を出すには？
  縁取りの方法

## ダイナミックフォントとビットマップフォント
