
# 学生のカリキュラムのアイディア

## CPUレベルのプログラムの話

### 16進数
- 2進数,10進数,16進数の説明
- 単位の話 バイトとビット
- 60進数は -> 時間

### アドレス
- メモリーはアドレスが割り振られている。

### 文字コード
- ASCII, Unicode, UCS-4の違いについて
- Unicodeでもコードが足りなくなってきた話
- UTF-8, UTF-16, UTF-32について
- ソースコードの保存時のエンコード形式

### CPUの歴史

##### 8ビット
- 6502
- 4004, 8080
- Z80

##### 16ビット
- 8086, 80186, 80286
- 68000

##### 32ビット
- 80386, 80486, Pentium

##### 64ビット
- Core 2 Duo , Core i3, Core i5, Core i7, Atomなど

<img width="400" src="http://livedoor.blogimg.jp/ocworks/imgs/1/c/1cd84e7d.png">


### CPUとゲーム機の対応表

#### intelのマイクロプロセッサ
WindowsPC, Mac, サーバーなど圧倒的なシェアを誇る

#### AMDのマイクロプロセッサ
intelCPU互換で、近年はゲーム機に採用されることが多い

- PS4, Xbox One etc

#### PowerPCのマイクロプロセッサ
- WillU, PS3 etc

#### ARMのマイクロプロセッサ
- iPhoneシリーズ, Nintendo DS or 3DS

ＣＰＵの実物や写真を見せて実際の部品のイメージを思い浮かべてもらう。

### 自分の使用しているPCのCPUを調べてみよう。
- Windows10 で調べ方を説明する。

### 現在でもほとんどのコンピュータがノイマン型

- 現在あるコンピューターのほとんどはノイマン型だという説明


### x86 と x64どちらが性能が良いか？
32ビット64ビットを分ける言い方としてx86とx64と表示することがある。
x86のほうが数字が大きいので こちらのほうが性能が良い気がするがx86は32bitを表します。
x64は64bitなので性能が高いのはx64です。

## CPUと周辺のハードウェア

## リトルエンディアンとビックエンディアン

## RISC と CISC
厳密な定義がないそうですが、こんな感じに覚えるのが良い。
命令とデータが固定サイズ例えば32ビットになっているのをRISC
サイズが違うのをCISCと定義する。

よって IntelのCorei7はCISCとなる。

## CPUクロックについて
Core i7 4.20GHz  : 4,200,000,000回 : 4.2億回

約1命令1クロックで処理する。

## CPUのソフトウェア

### レジスタ,メモリーなどのCPUレベルの話
  - 汎用レジスタ(a,b,c,d,e)
  - pcレジスタの役目
  - spレジスタの役目
  - Fレジスタ

### load / store

### 演算
  - 加減算
  - 比較
  - シフト命令
  - 論理演算
  - ビット演算

### ジャンプ、分岐命令
  - jp jz

### サブルーチン呼び出し
  - call,ret命令

### 待避・復帰命令
  - push,pop
     アルゴリズムで出てくるスタック構造です。

### 入出力命令
  - IN, OUT

### 割り込み
  - NMI, V-Blank

### メモリー
  - ROM
  - EPROM,EEPROM
  - DRAM
  - SRAM
  - フラッシュメモリー( MemoryStick Duo )

### CPUから出ているピン(端子)って何に使うの？
  - A0～A15(アドレスバス)、D0～D7(データバス)を説明してメモリーとやり取りする線だということを説明。
  - Z80のピンを図解して説明

### 大容量記憶装置
 - HDD と SSD

### バス
 - バンクメモリー
  - メモリーからデータを読む時にＣＰＵとRAMの動作

### IOポート

### マルチコアやマルチプロセッサー

### CPUの実行している様子のアニメーションを作ることができないか？

### VRAM(Video RAM)のお話し
 - CRTCコントローラーがモニターに画像として映し出す。

### コントローラーやキーボード
 - ボタンを押すと電流が流れ0になる。
 - チャタリング

## アセンブラの話
 - ld a,0 より xor aのほうが命令が短い。
 - 掛け算、割り算が出来ないのでシフトを使用する。
 - push,popを使ったスタック構造の話
 - ローカル変数という概念はあまりなく、グローバル変数を定義して直接保存していた。

## コンパイラの話
 - 最適化について
  - 少ない命令で表現する。
  - 実行速度を早くする。パイプラインを乱さない。

## リンカーの話


### C/C++言語でコードを書く理由

  現在でもゲーム業界はC/C++言語でプログラムを書いているプロジェクトは存在します。
  アクションゲームは特にフレームレートが大事でゲームの操作感に影響され
  ゲームの面白さと関連が出てくる。

  プログラマが直接アセンブラで記述することは少ない。
  C/C++で記述したコードがどのような機械語になっているかを確認する方法がある。

  その方法を学習したいと思います。

### デバッカーの使い方

- 変数の確認
- メモリー内容の確認方法
- ブレークポイントのつけ方
- ステップ実行してプログラムの動きをデバックする

### 最初のプログラムはmainから起動する？
- main関数の前に動いているプログラムがあることを説明

### Windows コンソールアプリケーションを作る

1. Visual Stduio 2019を起動します
1. メニューの[ファイル(F)]-[新規作成(N)]-[プロジェクト(P)...]を選択
1. [Visual C++]-[Windowsコンソールアプリケーション]を選択

```
    ファイル名(N): ConsoleApplication1
    場所(L): 任意
    ソリューションのディレクトリを作成(D) のチェックをつける
```

### 簡単なC言語のプログラムを逆アセンブラしてみよう

```C++
  #include <stdio.h>

  int main()
  {
      printf("Hello World!\n");
  }
```

### ソースコードにブレークポイントを設定
- int main()の横にマウスカーソルを合わせて赤いマークを付ける
  又はソースコードにカーソルを合わせ

```
    [メニュー]-[デバック]-[ブレークポイントの設定/解除]で設定します。
  　※F9 キーで設定可能です。
```

### Debugビルドして 逆アセンブルを確認
1. Debug と x86を選択して 開始又はローカルWindowsデバッカをを起動
1. ソースコード上でマウス右メニューで逆アセンブルへ移動を選ぶ。
1. 表示オプションのコードバイトの表示を✔をつける

以下の様に表示されます。
```
  int main()
  {
  00A61810 55                   push        ebp  
  00A61811 8B EC                mov         ebp,esp  
  00A61813 81 EC C0 00 00 00    sub         esp,0C0h  
  00A61819 53                   push        ebx  
  00A6181A 56                   push        esi  
  00A6181B 57                   push        edi  
  00A6181C 8D BD 40 FF FF FF    lea         edi,[ebp-0C0h]  
  00A61822 B9 30 00 00 00       mov         ecx,30h  
  00A61827 B8 CC CC CC CC       mov         eax,0CCCCCCCCh  
  00A6182C F3 AB                rep stos    dword ptr es:[edi]  
  00A6182E B9 02 C0 A6 00       mov         ecx,offset _001BD82A_consoleapplication1@cpp (0A6C002h)  
  00A61833 E8 DA F9 FF FF       call        @__CheckForDebuggerJustMyCode@4 (0A61212h)  
  	printf("Hello World!\n");
  00A61838 68 30 7B A6 00       push        offset string "Hello World!\n" (0A67B30h)  
  00A6183D E8 09 F8 FF FF       call        _printf (0A6104Bh)  
  00A61842 83 C4 04             add         esp,4  
  }
  00A61845 33 C0                xor         eax,eax  
  00A61847 5F                   pop         edi  
  00A61848 5E                   pop         esi  
  }
  00A61849 5B                   pop         ebx  
  00A6184A 81 C4 C0 00 00 00    add         esp,0C0h  
  00A61850 3B EC                cmp         ebp,esp  
  00A61852 E8 C5 F9 FF FF       call        __RTC_CheckEsp (0A6121Ch)  
  00A61857 8B E5                mov         esp,ebp  
  00A61859 5D                   pop         ebp  
  00A6185A C3                   ret  
  ```

### Releaseビルドして 逆アセンブルを確認

コードが最適化されているのがわかると思います。
```
  	printf("Hello World!\n");
  00AE1040 68 F8 20 AE 00       push        offset string "Hello World!\n" (0AE20F8h)  
  00AE1045 E8 C6 FF FF FF       call        printf (0AE1010h)  
  00AE104A 83 C4 04             add         esp,4  
  }
  00AE104D 33 C0                xor         eax,eax  
  00AE104F C3                   ret
```

### C言語のプログラムを逆アセンブラしてみよう（その２）
```C++
  #include <stdio.h>

  int main()
  {
      int number = 0x01234567;
      printf("number=%d", number );
  }
```
### Debugビルドして 逆アセンブルを確認
```
  #include <stdio.h>
  #include <memory.h>

  int main()
  {
  010E42F0 55                   push        ebp  
  010E42F1 8B EC                mov         ebp,esp  
  010E42F3 81 EC CC 00 00 00    sub         esp,0CCh  
  010E42F9 53                   push        ebx  
  010E42FA 56                   push        esi  
  010E42FB 57                   push        edi  
  010E42FC 8D BD 34 FF FF FF    lea         edi,[ebp-0CCh]  
  010E4302 B9 33 00 00 00       mov         ecx,33h  
  010E4307 B8 CC CC CC CC       mov         eax,0CCCCCCCCh  
  010E430C F3 AB                rep stos    dword ptr es:[edi]  
  010E430E B9 0A C0 0E 01       mov         ecx,offset _001BD82A_consoleapplication1@cpp (010EC00Ah)  
  010E4313 E8 FA CE FF FF       call        @__CheckForDebuggerJustMyCode@4 (010E1212h)  
  	int number = 0x01234567;
  010E4318 C7 45 F8 67 45 23 01 mov         dword ptr [number],1234567h  
  	printf("number=%d", number);
  010E431F 8B 45 F8             mov         eax,dword ptr [number]  
  010E4322 50                   push        eax  
  010E4323 68 30 7B 0E 01       push        offset string "number=%d" (010E7B30h)  
  010E4328 E8 1E CD FF FF       call        _printf (010E104Bh)  
  010E432D 83 C4 08             add         esp,8  
  }
  010E4330 33 C0                xor         eax,eax  
  010E4332 5F                   pop         edi  
  010E4333 5E                   pop         esi  
  010E4334 5B                   pop         ebx  
  010E4335 81 C4 CC 00 00 00    add         esp,0CCh  
  010E433B 3B EC                cmp         ebp,esp  
  010E433D E8 DA CE FF FF       call        __RTC_CheckEsp (010E121Ch)  
  010E4342 8B E5                mov         esp,ebp  
  010E4344 5D                   pop         ebp  
  010E4345 C3                   ret  
```
### Releaseビルドして 逆アセンブルを確認
```
  	int number = 0x01234567;
  	printf("number=%d", number);
  00F71040 68 FF 00 00 00       push        1234567h  
  00F71045 68 F8 20 F7 00       push        offset string "number=%d" (0F720F8h)  
  00F7104A E8 C1 FF FF FF       call        printf (0F71010h)  
  00F7104F 83 C4 08             add         esp,8  
  }
  00F71052 33 C0                xor         eax,eax  
  }
  00F71054 C3                   ret
```

## GPUレベルのプログラムの話
 - 描画バッファと表示フレームバッファ
　- 描画バッファをr,g,b,aのメモリーレベルで理解してもらいどのようにディスプレーに表示しているかを理解してもらう。
 - ディスプレーバッファ
 - 頂点、法線、頂点カラーデータを用意する
 - 陰影と頂点カラーの仕組み
 - アフィン変換の仕組み
 - テクスチャーマッピング
  - VirtuaFighter から VirtuaFighter2の変化
 - Unityを使ったサンプル

## 業務ツールの活用
 - Git
  - GitLFSを使い大容量ファイルを扱う
 - GitHub or GitLab
  - ブランチ
  - プルリクエストの行い方
 - SourceTreeの活用
 - Chatwrork, Slackなどのコミュニケーションツールの活用。
  - Skype,Facebookではだめなのか？
 - Webベース・チケット作業
  - wiki, issueの活用
  - jira, readmine, gitHub-issueなど Webでチケットシステムで開発していくノウハウ
 - 社内イントラネットを作る
  - 社員リストが参照できる
  - 社内プロジェクト一覧
 - メール
 - Cloud サーバー
  - Googleドライブ, dropbox などたくさんあるクラウドサービスでどのように作っていくかを構築。
 - 自動テスト環境を構築
  - JenkinsやDevOpsなどを活用した自動テスト環境を構築
  - デイリービルドを必ず行い、誰でも簡単にアプリが落とせるようにしておくこと
  - チャットワーク, slackなどにビルド結果を通知
 - ソフトウェアライセンス管理
 - スマホなどの貸し出し機材の確認
 - 情報漏えいが発生しないような管理と運営


## アプリの制作からAndroidに転送実行

- Unityでのアプリの作り方
- 実行テスト
- アプリ転送
- Visual Stduio 2019でブレークポイントを設定


## Unity リアルタイムレンダリング映像制作
1. Unity TimeLineで映像制作( 社内チーム )
1. ここで制作した人が先生となり専門学校で授業
1. Unity TimeLineで映像制作( 専門学校学生チーム )
1. 卒業制作をリアルタイムレンダリング映像

### 学べること
 - Git, GitLFS, GitHub, SourceTree, Unity Timeline, Unity FBX Exporter, ShaderGraph, Visual Effect Graph

### Unityを活用して映像制作をしてみること
 - ゲームのリアルタイムムービーシーンに活用する
 - 3DデザイナーのUnityを扱う知識が蓄積
  - モデリングの知識
  - マテリアル制作
  - Unity ShaderGraphの知識
 - テクニカルアーティストの育成
  - Unity ShaderGraphの知識

### 対象の学生
- ３Dデザイナ
- Shaderプログラマ
- テクニカルアーティスト

## プロのゲームプログラマとして心構え
 - 制作にはリソース、予算と期間があること
  - どのように予算内、期間内に作るか？
 - 制限のある状態（期間と予算）で最高のものを作る。
