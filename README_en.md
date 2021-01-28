# Unreal Engine 4 Third Person Sprite Project (TPSprite)
English README

Created VersionUE4(Win)　4.25.4　(Blueprint Project)


## Introduction
The Unreal Engine 4 Third Person Sprite Project is a bit long, so we'll call it TPSprite.

The 3D model of the third person template has been replaced with a 2D image.

Also, since the author is not familiar with GitHub, please point out to us if we have deviated from the etiquette.

## Features
By simply preparing a 2D image, you can move the character in 3D space.

![TPSprite2](https://user-images.githubusercontent.com/62424367/106193927-81586a80-61f1-11eb-9eb9-da26bba331b7.gif)

The minimum material required is four images: front, left, right, and back.

![gray_idle_4way](https://user-images.githubusercontent.com/62424367/106199342-a6041080-61f8-11eb-9e9d-4c766d37dc5f.png)

An 8-way image makes for a slightly richer picture creation. (It's hard to make many of them)

![gray_idle](https://user-images.githubusercontent.com/62424367/106199357-ad2b1e80-61f8-11eb-9474-bc1a0762eda1.png)

## Operating environment
- UE4.25 or later
- I'm working on Windows, can I share it with Mac?
- The Config data in the Save folder is included to take advantage of the folder's color specification.
- It's just a basic function, so it will work on any environment that can run regular UE4.

## How to use
- First, download

![TPSprite_download2](https://user-images.githubusercontent.com/62424367/106183353-75fe4280-61e3-11eb-8b74-b1c2e51bba05.jpg)

- Answer the Zip in the place where you usually keep your UE4 project and double-click on the project data to open it.

![TPSprite_003](https://user-images.githubusercontent.com/62424367/106184384-cfb33c80-61e4-11eb-8abc-1ca02876bae7.jpg)

- You can also open it from the Epic launcher.

![TPSprite_004](https://user-images.githubusercontent.com/62424367/106185900-d773e080-61e6-11eb-9e6d-671cca8a18b1.jpg)

- The main part of this process will be this ThirdPersonSprite4way (4 directions) and ThirdPersonSprite8way (8 directions).

![TPSprite_005](https://user-images.githubusercontent.com/62424367/106186737-0179d280-61e8-11eb-9fb2-f43d51b63993.jpg)

- This video production is processed with Tick. (The smoother it is, the better it looks in the video.)
- If you are concerned about the processing speed, use Timer by Event instead of Tick.
- Also, when I tried to make the camera face the direction of the Material, the shadows didn't follow, so I made it a CPU-side process.
- If you don't want shadows, you can use the included material instead of the Sprite To Camera function.
- The data for NPCs is a Timer, which changes the processing speed depending on the distance.
- Double-click on the function UpdateFlipbook to open it.

![TPSprite_006](https://user-images.githubusercontent.com/62424367/106187779-697ce880-61e9-11eb-8ea6-cfbc88c0d324.jpg)

- If you select Flipbook in the Select tab, the image will be replaced.
- If you do not know how to create a Flipbook, please check the link below.
  - [A collection of tips for making 2D dot art games in UE4. - Qiita](https://qiita.com/O_Y_G/items/cc1b4920a2b4a6bfd921)
  - [Let's make a UE4 2D action game #1 Dot-drawn characters -YouTube](https://youtu.be/fo3xTxEyq-w)

I'll try to explain it in a video in a little while.

## Sample images
![TPSprite_007](https://user-images.githubusercontent.com/62424367/106200576-88d04180-61fa-11eb-9da4-0b379251f0da.jpg)

- In the Sample folder, you will find the character images I used this time, so if you write these numbers by hand, it will be done. (Very hard)
- We recommend that you start by preparing only four IDLE images and try replacing them.
- Note that the dotted version of Gray Man was exported using this tool.
  - [3D to Pixel: Blueprints - UE Marketplace](https://www.unrealengine.com/marketplace/ja/product/3d-to-pixels)

## License
It will be released as fully public domain.

https://github.com/O-Y-G/TPSprite/blob/main/LICENSE

## Release History
- 2021/01/29 public

## In closing
As for the GitHub data upload, I was able to figure it out with [**関サヴァイヴァー**さん](https://twitter.com/seki_survivor/status/1354034438389129216?s=20)'s help.

In creating this README, we have used the
- [**Alwei**さんの**PPCelShader**](https://github.com/alwei/PPCelShader)
- [**はるべぇ**さんの**VRM4U**](https://github.com/ruyo/VRM4U)
- [**Mignon Style**さんの**Markdown記法 チートシート**](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)
- [**akiyoko**さんの**GitHub の Wiki に画像を貼り付ける一番簡単な方法（Wiki リポジトリを clone しないバージョン）**](https://akiyoko.hatenablog.jp/entry/2016/08/30/051708)

I created this file based on

Thanks again for sharing the info!

This project was kind of made in response to a question from [**KU**さん](https://twitter.com/KUforRPGmv), and I don't have any plans to use it myself at the moment, 

so I'd be happy if someone could use this project as a reference to make something fun.

It would be great to see a future that didn't lean towards 3D characters from the days of PS1.

## author
[@O_Y_G](https://twitter.com/O_Y_G)
