# myled2

# ロボットシステム学2021年度課題1
このプログラムは上田隆一先生が担当する2021年ロボットシステム学の課題1で作成したものである.

講義動画[1]内で上田先生が作成したプログラムを参考にしてプログラムを作成したもの[2]を前提に, 自分で内容を考えてオリジナルのプログラムを製作した

## ●プログラムの概要
使用者が実行する際に　 echo [] > /dev/myled0　の[]内に打ち込んだ英文字の通りにLEDがモールス信号で点滅するプログラムである.

## ●動作環境

・Rasberry Pi 4 

・Os : Ubuntu 20.04 server

## ●使用したもの 

・Rasberry Pi 4 

・LED(赤) x 1 

・抵抗 220Ω x 1 

・ブレッドボード BB-601(白) x 1 

・ジャンパー線 x 1


## ●使用方法

###【インストール】 
```
$ git clone https://github.com/yuikadomura/myled2.git

$ cd myled2 

$ make 

$ sudo insmod myled.ko 

$ sudo chmod 666 /dev/myled0
```

###【アンインストール】 
```
$ sudo rmmod myled 

$ make clean
```

###【LEDを入力した文字の通りにモールス信号で点灯させる】 
```
$ echo [ 任意の英文字or英単語 ] > /dev/myled0
```
※対応しているのはA～Z, a～zのアルファベットであり, 特に文字数に制限はない. 
※実際に上記のコマンドを打ち込む際に[]は必要ない.

## ●モールス信号について

モールス符号は, 電信で用いられている可変長符号化された文字コードで, 
そのモールス符号を使った信号がモールス信号である.


## ●実行時の動画 

Youtubeのリンクは[こちら]()

## ●参考

[1] [第7～8回講義動画](https://youtu.be/xQW8-FNuboo)

①Readme の書き方について[こちらのサイト](https://style.potepan.com/articles/33682.html#GitHubREADME-3)

②上田隆一先生の講義動画[第3回補足](https://youtu.be/vjiWa3srH7g)と[講義動画](https://ryuichiueda.github.io/robosys2020/lesson7_device_driver.html#/)7のスライド

③武蔵ツールズ[こちらのサイト](https://musashitools.com/instrument/%e3%83%a2%e3%83%bc%e3%83%ab%e3%82%b9%e7%ac%a6%e5%8f%b7%e3%81%ae%e6%97%a9%e8%a6%8b%e8%a1%a8%e3%83%bb%e4%b8%80%e8%a6%a7%e8%a1%a8/#alpha)

を非常に参考にさせていただいたため感謝しています.

