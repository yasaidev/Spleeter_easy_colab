#どこにあるか

[ここ](https://colab.research.google.com/drive/1EjysPW--w5a-NuQHkiCjL3mZg8y7Zdey)においてあるので使ってみてください．GPUを使用するので処理速度がかなり早いです．ただでGPU貸してくれるGoogle最高！！

#使い方

エラーが出たらランタイムの再起動をして，準備の章からセルを一つずつ実行し直してください．そうすれば，大概のエラーは解決すると思います．
もし，download時にnetwork〰なエラーが出る場合はもう一度そのセルを実行し直してください．ファイルの生成のタイミングによって発生するようです．ブラウザーをChromeに変えるとエラーが出ないかもしれないです．

##準備
###プログラムの読み込み

はじめに，[このノート](https://colab.research.google.com/drive/1EjysPW--w5a-NuQHkiCjL3mZg8y7Zdey)をplaygroundモードで開いてください．画面上部にあります．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/04d10297-d5c3-a18d-6e76-a797578a5609.png)
次に「準備」の章のセルをすべて実行(ctrl+enter)してください．
そして，「モジュール・メソッドの読み込み」の章のセルを実行(ctrl+enter)してください．

実行は下の写真のような各セルの[　]をクリックしてもできます．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/19e72f8f-5eaf-0bc3-fd49-fd6a132e8a12.png)

###曲の準備

「分割したい曲をここからアップロード」のところのセルを実行すると，以下のような表示がされるので，参照をクリックして任意の音源をアップロードしてください．<font color="Red">__複数の音源をアップロードする場合でも毎回このセルを実行し直してください．__</font>
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/95e84f20-48fb-b90a-081f-e286ccc3b773.png)
以下の画像のようになったら，ファイルのアップロードが完了です．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/12b23110-5c93-0d0a-cb36-b658d1db4786.png)

また，複数の音源を同時にアップロードする場合などは，左タブの「ファイル」で表示されているフォルダにて「アップロードボタン」をクリックや，タブにドラッグアンドドロップして，ファイルをアップロードする方法もおすすめです．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/faa32c31-f908-a5e0-b84a-95859230619f.png)

<font color="Red">__曲を追加したとき，視聴などにその曲を反映させるには，視聴などのセルをもう一度読み直してください．__</font>

##視聴

視聴をするには視聴の章のセルを実行してください．しばらくすると以下のように表示され，視聴が可能です．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/cbd70c60-09de-eb50-7074-dd7728455a10.png)
##分割して曲をダウンロード
zipでも一つずつでもダウンロードできます．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/d8705511-d16d-b136-d04c-21e792f6e44a.png)

##各パートを合成してダウンロード

ドラム抜き音源やボーカルオフ音源などを作るにはこのブロックを利用してください．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/07852b0d-5e59-2174-00cb-323200ba3b89.png)

##既知のバグ

Downloadや視聴がときどき二回分実行されてしまう不具合があります．一応ランタイムの再起動をすると治ります．ただし，根本的な原因がわからないのと実用上問題はないので放置しています．どなたか原因がわかる方いたら教えて下さい．おそらくスコープの扱いがまずいので起こっている気がします．勉強して直すようにしたいです．

#もっといいもの

とりあえずSpleeter使ってみたいけど，Google ColabやPythonが苦手な方は[splitter.ai](http://www.splitter.ai/)を使うことをおすすめします．すごくわかりやすいインターフェイスが実装されています．ただし，サーバー側で分割作業をおこなっているようなので，待ち時間が必要となるそうです．
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/204520/5b54d499-81fa-9bba-dc3a-5b9c96705b8d.png)

#Spleeterとは

[Github](https://github.com/deezer/spleeter)ページのAbout欄に書いてあることから抜粋すると，深層学習を利用して一つのミキシング済みの音源（いわゆる我々が日常的に聞く音楽）からボーカル，ドラム，ピアノ，ベース，その他楽器の最大5パートに分割してくれるライブラリーです．

#所感

耳コピをする人やコピーバンドの練習などに役立ちそうだと感じています．コマンドラインをこねくり回したくなかったのでGoogle colaboratoryに書いてみました．
