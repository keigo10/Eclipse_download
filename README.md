  
># みんちゅう環境構築手順書
　　

みんちゅうの環境構築手順書になります。  
この手順書を見ながら環境構築を行い、それでもわからないときは近くの先輩に尋ねましょう。

## ①Eclipseを導入する。

### Eclipseとは  


EclipseとはIBMが開発したオープンソースのIDE（統合開発環境）のことで、主にJavaの開発で使われます。  
開発効率を上げ、プログラマーの負担を軽減してくれる開発ソフトです。

### インストールする


Eclipseをダウンロードするために、[ここ]をクリックしてダウンロードページを開き、「Eclipse 2020」を選択してください。  

[ここ]:https://mergedoc.osdn.jp    
![image18](https://user-images.githubusercontent.com/57954776/93303112-f4120c00-f835-11ea-88fc-5c15bc2d8b98.png)  

続いて、「Java Full Edition」をダウンロードしてください。
なお、Full EditionにはJavaが内蔵されています。手っ取り早く作業を始めるにはFull Editionが便利です。

![image12](https://user-images.githubusercontent.com/57954776/93303835-06407a00-f837-11ea-83d8-312b3379e5af.png)  

ダウンロードが終了したら、ダウンロードしたファイルをクリックして、Eclipseを起動します。  
Windowsで開く場合は7-zipで解凍してください。7-zipをダウンロードしていない場合、
[これ]を見ながらダウンロードして下さい. 

[これ]:https://itojisan.xyz/  

解凍先したフォルダー内に「eclipse」フォルダーがありますので、その中の「eclipse.exe」を実行するとEclipseが起動します。

![image14](https://user-images.githubusercontent.com/57954776/93306213-861c1380-f83a-11ea-818d-f534d39be31d.png)  

階層が深いフォルダに保存すると起動しないことがあります。その場合は、保存する階層を浅くして下さい。
インストーラーを使わない場合は、デスクトップやWindowsのメニューにEclipseのショートカットは作成されませんので、この実行ファイル「eclipse.exe」のショートカットをデスクトップなどに作成しておくと便利です。
以下のような画面が表示されたら、導入成功です。  
  
<img src="https://user-images.githubusercontent.com/57954776/93306556-03478880-f83b-11ea-8138-44c09107448c.png" width="850px" height="500px">  
  
## ②EqlipseでGitを使えるようにする。

### Gitとは  

Git（ギット）は、プログラムのコードなどを変更した際、その履歴を記録・追跡するシステムです。  

開発会社や事業会社のIT部門などで利用されており、プログラマーだけでなくデザイナーや、企業によっては一般部門でも利用が広がっています。

### なぜ管理する必要があるのか

そもそも、なぜ変更の履歴を管理する必要があるのか考えてみましょう。  
ファイルを作成しているとき、以前の内容を確認したくなったり、数日前の状態に戻したくなったことはありませんか？  
その場合、みなさんはどのようにしていますか？  


よく見かける手軽な方法は、編集前のファイルを事前にコピーしておく方法ではないでしょうか。
ファイル名に、日付やバージョンなどを追加しておくことが多いと思います。  
  
  
![image4](https://user-images.githubusercontent.com/57954776/93310962-596afa80-f840-11ea-9d53-8e7ffe7ada19.png)
  
  
しかし、無秩序に更新を重ねていくと、最新版が区別できなくなってしまう恐れがあります。
また、変更した内容を知るには、前後のファイルを一つひとつ比較しなければなりません。
さらに、他者と共有してファイルを編集している場合、同時に編集して変更内容が消えてしまったり、誤って上書きしてしまうこともあるでしょう。
Gitのような変更履歴(バージョン)を管理するシステムは、これらの不便を解消し、次のような作業を容易にします。

- 変更点を知る  
- 誰が、なぜ変更したのか記録する  
- 以前の状態に戻す  
  
***

### Eclipseにプラグイン「EGit」のインストール  
  
  
まずは、EclipseにGitを使うためのプラグイン「[EGit]」をインストールしましょう。  
「ヘルプ」⇒「新規ソフトウェアのインストール」からインストールウィンドウを開きます。  

<img src="https://user-images.githubusercontent.com/57954776/93313639-b3b98a80-f843-11ea-8f32-d8f2bf4ac20d.png" width="400px" >  

[EGit]:https://www.eclipse.org/egit/  
  
右上の「追加」を押し、名前に「EGit」、ロケーションに「`http://download.eclipse.org/egit/updates`」を入力し「追加」を押します。  

<img src="https://user-images.githubusercontent.com/57954776/93315781-6a1e6f00-f846-11ea-9ca1-d6b3da0407ed.png" width="600px" > 

一覧が表示されるので、すべてチェックを入れて「次へ」を押します。  
  
  <img src="https://user-images.githubusercontent.com/57954776/93316347-08123980-f847-11ea-9879-fc61c6f457d0.png" width="600px" >

インストールするものの一覧が出るのでそのまま「次へ」を押します。  
  
  <img src="https://user-images.githubusercontent.com/57954776/93316761-94246100-f847-11ea-80e9-d6afeb632c90.png" width="600px" >

利用規約に同意し「完了」を押すとインストールが実行されます。  

 <img src="https://user-images.githubusercontent.com/57954776/93317081-fc734280-f847-11ea-925d-6cf0c710397e.png" width="600px" >

しばらくするとEclipseの再起動を促されるので、再起動すればインストール完了です。


## ③A5:SQL Mk-2を導入する。

### A5:SQL Mk-2のインストール

「A5:SQL」 とは
公式サイトには「 高機能かつ軽量な汎用SQL開発ツール」と書かれています。
本当にその通りで、SQL、データベース回りの開発でやりたいことが
汎用的になんでもできる、高性能なツールです。
 ※Windows専用ソフトなのでMacでは使えません。

[A5:SQL Mk-2]をインストール。  

[A5:SQL Mk-2]:https://a5m2.mmatsubara.com/

<img src="https://user-images.githubusercontent.com/57954776/93318857-2594d280-f84a-11ea-9ebd-77964c093798.png" width="600px" >

MySQLのインストール
MySQLをダウンロードしていない方はここ（https://webkaru.net/mysql/install-windows/
）を見ながらインストールをしてください。  
※この記事はMySQLのバージョンが古いため、少し違った内容のものもございます。調べながらインストールを行い、それでもわからないときは周りの人に聞きましょう。

## A5:SQL Mk-2をMySQL serverに接続する  
  
  A5:SQL Mk-2 は MySQL Server に接続する際に、MySQL ClientがクライアントPC（A5:SQL Mk-2のインストールされているPC）にインストールされている必要はありません。

　A5:SQL Mk-2 は MySQL Server に対してMySQLのクライアントライブラリを利用せず直接接続します。クライアントライブラリを経由した接続はGPLの問題からサポートしません。

　この説明で使ったソフトウェアのバージョンは以下のとおりです。

MySQL 5.0.51a-community-nt
A5:SQL Mk-2から「データベースの追加と削除」スピードボタンを押下します。

<img src="https://user-images.githubusercontent.com/57954776/93318963-45c49180-f84a-11ea-9b46-24a338788e68.png" width="600px" >   

データベースの追加と削除ダイアログで、「追加」ボタンを押下します。  

<img src="https://user-images.githubusercontent.com/57954776/93319058-6391f680-f84a-11ea-8ff8-e8a37a2575d2.png" width="600px" > 

「MySQL (直接接続)」ボタンを押下します。  

<img src="https://user-images.githubusercontent.com/57954776/93319169-83c1b580-f84a-11ea-9047-18c8a388cab8.png" width="600px" >  

ホスト名・ポート番号・ユーザーID・パスワード・データベースを入力します。   
必要に応じて「パスワードを保存する」にチェックを入れます。  
「データ交換に Unicode を利用する」・「メタデータ（テーブル名・カラム名・コメント）取得に Unicode を利用する」は文字化け等問題が発生する場合のみ変更して下さい。  
全て入力したら、「OK」をクリックします。  

<img src="https://user-images.githubusercontent.com/57954776/93319272-a358de00-f84a-11ea-824a-7dfd9bc5a1e9.png" width="600px" >  

データベース別名（A5:SQL Mk-2の中でデータベースを一意に識別する名前）を入力し、「OK」を押下します。

<img src="https://user-images.githubusercontent.com/57954776/93319468-dac78a80-f84a-11ea-8a33-955eca473bc1.png" width="600px" >  

「閉じる」を押下します。  

<img src="https://user-images.githubusercontent.com/57954776/93319553-f6cb2c00-f84a-11ea-87f3-59d9237cfb0e.png" width="600px" >  

データベースツリーから登録したデータベースをダブルクリックして接続します。

<img src="https://user-images.githubusercontent.com/57954776/93319596-05b1de80-f84b-11ea-8ec1-43083268f5d2.png" width="600px" >  

ユーザーIDとパスワードを指定し、「OK」を押下して接続します。

<img src="https://user-images.githubusercontent.com/57954776/93319667-1c583580-f84b-11ea-898d-d12892769314.png" width="600px" >   

次のようになれば接続成功です。

<img src="https://user-images.githubusercontent.com/57954776/93319751-33972300-f84b-11ea-8577-0077f06f5147.png" width="600px" >   
