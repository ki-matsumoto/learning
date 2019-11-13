# DOTweenを使用してみよう
<div style="text-align: right;">
2019年11月13日<br>
株式会社アルファオメガ  松本清明
</div>


# DOTweenのインストール

## DOTween 公式サイト

<img width="640" alt="DOTween" src="img/04/DOTween.png">

[DOTween公式サイト](http://dotween.demigiant.com/)

## DOTween アセットのダウンロード

<img width="640" alt="DOTween_Download" src="img/04/DOTween2.png">

[Downloadサイトのリンク](http://dotween.demigiant.com/download.php/)

最新版 v1.2.305(2019/11/13現在)です。
DOTween_1_2_305.zipをダウンロードしてくだください。
又はダウンロードしてコピーしてありますので使用してください。

## インストール方法

## 新規プロジェクトをつくります
<img width="480" alt="Unity1" src="img/04/Unity1.png">

## Unityの起動画面
<img width="480" alt="Unity2" src="img/04/Unity2.png">

### DOTween_1_2_305.zipの解凍
- DOTween_1_2_305.zipを展開して出てきたDOTweenフォルダーをUnityプロジェクトの Assetsにコピーします。

### Unityにインポート
<img width="480" alt="Unity3" src="img/04/Unity3.png">
- 以下のダイアログが表示されます。

<img width="320" alt="DOTween3" src="img/04/DOTween3.png">
- Open DOTween Unity Panelボタンを押します。

### DOTween Unity Panel ダイアログ
<img width="320" alt="DOTween4" src="img/04/DOTween4.png">
- 緑のボタンのSetup DOTween...を押します。


### DOTween Unity Panel ダイアログ
<img width="320" alt="DOTween5" src="img/04/DOTween5.png">
- Applyを押します。
これでDOTweenが使用できるようになりました。


# DOTweenを使用してみよう

## シーンを作成

### Plane GameObjectを配置
### Plane のマテリアルを変更
### cube GameObjectを配置
### Cameraを変更

<img width="640" alt="Unity5" src="img/04/Unity5.png">

- 確認しやすいようにカメラを変更します。

例)

|パラメータ|X|Y|Z|
|:--|:--|:--|:--|
|Postion|0|5|-6|
|Rotation|42|0|0|
|Scale|1|1|1|

## Sample.csを作成
Sample.cs
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using DG.Tweening;

public class Sample : MonoBehaviour {

	[SerializeField]
	GameObject CubeGameObject;

	// Use this for initialization
	void Start () {

	}

	// Update is called once per frame
	void Update () {

	}

	public void OnButtonDown()
	{
		this.CubeGameObject.transform.DOMove(new Vector3(3.0f, 0.5f, 0), 2.0f);
	}
}
```

## Canvasにsample.csスクリプトを割り当てる
<img width="640" alt="Unity7" src="img/04/Unity7.png">
- 画像の赤の部分の様にCube GameObject のインスタンを設定します。


## ボタンに関数を割り当てる

<img width="640" alt="Unity8" src="img/04/Unity8.png">

- 画像の赤の部分の様にCanvasのオブジェクトを割り当ててSample.OnButtonDown関数を設定します。


# 最後に
色々なTweenがありますので、改造して色々な動きを作ってみて下さい。
