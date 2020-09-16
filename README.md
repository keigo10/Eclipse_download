  
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
