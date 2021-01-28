# Unreal Engine 4 Third Person Sprite Project (TPSprite)
English README

作成バージョンUE4(Win)　4.25.4　(Blueprint Project)


## はじめに
Unreal Engine 4 Third Person Sprite Project は、ちょっと長いので以下　TPSpriteとします。

サードパーソンテンプレートの3Dmodelを、2D画像に差し替えたものになります。

また、製作者は、GitHubに不慣れなため、作法から逸れたことをしていた場合は、ご指摘いただければと思います。

## 特徴
2D画像を用意するだけで、3D空間上でキャラクターを動かすことができます。

![TPSprite2](https://user-images.githubusercontent.com/62424367/106193927-81586a80-61f1-11eb-9eb9-da26bba331b7.gif)

最低限必要な素材は、正面　左右　後ろ姿　の4枚の画像が必要です。

![gray_idle_4way](https://user-images.githubusercontent.com/62424367/106199342-a6041080-61f8-11eb-9e9d-4c766d37dc5f.png)

8方向の画像があると、少しリッチな絵作りになります。(たくさん作るのは大変です）

![gray_idle](https://user-images.githubusercontent.com/62424367/106199357-ad2b1e80-61f8-11eb-9474-bc1a0762eda1.png)

## 動作環境
- UE4.25以降
- Windowsで制作していますが、Macと共有できるんですかね？
- SaveフォルダのConfigデータは、フォルダの色指定を生かしたい為入れてあります。
- 基本機能だけなので、通常のUE4が動く環境であれば、動くと思います。

## 使い方
- まずダウンロード

![TPSprite_download2](https://user-images.githubusercontent.com/62424367/106183353-75fe4280-61e3-11eb-8b74-b1c2e51bba05.jpg)

- いつもUE4プロジェクトを置いてる場所にZipを解答し、プロジェクトデータをダブルクリックで開く。

![TPSprite_003](https://user-images.githubusercontent.com/62424367/106184384-cfb33c80-61e4-11eb-8abc-1ca02876bae7.jpg)

- Epicランチャーから開いてもいいです。

![TPSprite_004](https://user-images.githubusercontent.com/62424367/106185900-d773e080-61e6-11eb-9e6d-671cca8a18b1.jpg)

- 今回の処理のメインは、こちらのThirdPersonSprite4way（4方向）とThirdPersonSprite8way（8方向）になります。

![TPSprite_005](https://user-images.githubusercontent.com/62424367/106186737-0179d280-61e8-11eb-9fb2-f43d51b63993.jpg)

- 今回の動画制作は、Tickで処理をしています。(滑らかな方が、動画的に見栄えが良い為)
- 処理速度が気になる場合は、Tickの代わりにTimer by Eventなどで代用してください。
- また、Materialでカメラ方向を向かせようとすると、影がついてこなかった為CPU側の処理にしています。
- 影がいらない場合は、同梱のマテリアルを、Sprite To Camera　の関数の代わりに使うといいと思います。
- NPC用のデータは、Timerで、距離に応じて処理速度が変わるようになっています。
- 関数　UpdateFlipbookをダブルクリックで開いてください。

![TPSprite_006](https://user-images.githubusercontent.com/62424367/106187779-697ce880-61e9-11eb-8ea6-cfbc88c0d324.jpg)

- Selectのタブに、Flipbookをしていすれば、画像が差し変わります。
- Flipbookの作成方法が分からないかたは、下記のリンクをご確認ください。
  - [UE4で2Dドット絵ゲームを作る際のTipsまとめ。 - Qiita](https://qiita.com/O_Y_G/items/cc1b4920a2b4a6bfd921)
  - [UE4 2Dアクションゲームを作ろう #1 ドット絵キャラクター編 -YouTube](https://youtu.be/fo3xTxEyq-w)

少ししたら、動画で説明しようと思います。

## Sample画像
![TPSprite_007](https://user-images.githubusercontent.com/62424367/106200576-88d04180-61fa-11eb-9da4-0b379251f0da.jpg)

- Sampleフォルダに今回使ったキャラクター画像があるので、手書きでこの枚数書くと、出来上がります。（大変）
- まずはidle画像を4枚だけ用意して、差し替えてみることをお勧めします。
- なお、今回のグレイマンのドット化は、こちらのツールを使って書き出したものになります。
  - [3D to Pixel：ブループリント - UE マーケットプレイス](https://www.unrealengine.com/marketplace/ja/product/3d-to-pixels)

## ライセンス
完全なパブリックドメインとして公開します。

https://github.com/O-Y-G/TPSprite/blob/main/LICENSE

## リリース履歴
- 2021/01/29 公開

## おわりに
GitHubのデータアップロードに関しては、[**関サヴァイヴァー**さん](https://twitter.com/seki_survivor/status/1354034438389129216?s=20)に教えてもらって、なんとかなりました。

こちらのREADMEを作成にあたっては、
- [**Alwei**さんの**PPCelShader**](https://github.com/alwei/PPCelShader)
- [**はるべぇ**さんの**VRM4U**](https://github.com/ruyo/VRM4U)
- [**Mignon Style**さんの**Markdown記法 チートシート**](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)
- [**akiyoko**さんの**GitHub の Wiki に画像を貼り付ける一番簡単な方法（Wiki リポジトリを clone しないバージョン）**](https://akiyoko.hatenablog.jp/entry/2016/08/30/051708)

を参考に、作成させていただきました。

いつも情報共有感謝します！

このプロジェクトは[**KU**さん](https://twitter.com/KUforRPGmv)からの質問に答える形で、なんとなく作ったプロジェクトで、今のところ自分で使う予定がないので、

誰か、このプロジェクトを参考に、楽しいものを作ってくれたら嬉しいです。

PS1の時代から3Dキャラクターに傾倒しなかった未来を見れたら嬉しいです。

## 作った人
[@O_Y_G](https://twitter.com/O_Y_G)
