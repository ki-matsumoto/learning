# CPU処理速度について
<div style="text-align: right;">
2019年11月30日<br>
株式会社アルファオメガ  松本清明
</div>

## できるだけ早く実行する意味
* 一秒って一瞬だよね。でもゲームプログラムにとっては長い時間

    60フレームのゲームを作るには約0.017秒よって17msで処理することになる。

    ※ちなみに１秒は1000ms.

    アニメーションは 1/24コマと言われています。(実際は業界に詳しくないのでわかりませんが)

    プログラムの処理を書く場所によっては処理速度はとても重要。

    アクションゲームを作るプログラムはこのような時間単位にプログラム処理速度を考える。


## プログラムの処理時間を気にしてプログラムをすることが大事


### clock関数を使用する

```c
#include <stdio.h>
#include <time.h>

using namespace std::chrono;

int main()
{
  // 計測スタート時刻を保存
  clock_t start = clock();
  //
  //　ここに処理プログラムを記述する
  //
  // 計測終了時刻を保存
	clock_t end = clock();
  // 要した時間を計算
	clock_t t = end - start;
  // ミリ秒に計算
	const double time = t / CLOCKS_PER_SEC * 1000.0;
  // ミリ秒で表示
	printf("time %lf[ms]\n", time);
	return 0;
}
```

## Visual Studio 2019でのプロファイル

大きなプログラムのボトルネックを調べるのには以下のようなプロファイラーを
使用して調べることもある。

[CPU 使用率を分析することでアプリケーションのパフォーマンスを測定する](https://docs.microsoft.com/ja-jp/visualstudio/profiling/beginners-guide-to-performance-profiling?view=vs-2019)
