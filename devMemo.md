## 個人的な開発メモ

***
### 開発した際の話

#### VScodeを使う人へ
普通にやめた方がいいです。IntelliJとやろうとすると整合性を取るのが本当に厳しい。  
特にimlファイル関係や自動ファイル生成が多く、使用に耐えるものじゃない。  
IntelliJは本当に終わってる。  

#### 現在の環境
外部パッケージは情報が錯綜していてよくわかっていない。
[こういうサイト](https://qiita.com/hideo9080/items/80abd75fa6f3cdeff6ea)でIntteliJの
外部パッケージの追加の仕方が紹介されているものの、
我々の環境はIntelliJ+Maven+JavaEEであるので、鵜呑みにするべきではない。  
Mavenでの追加方法は[これ](https://qiita.com/neko_the_shadow/items/2d5b82c04dc109ebc0ee)とか読んだけど、
書き方が良くわからんのでもっと調べて、[IDの話](https://code-macchiato.com/tips/maven-groupid-artifactid)とか見て書いた。

そうすると次はmodule-info.java(JavaEE)の問題が出てきて……よくわからない。  
たぶん使うパッケージを制限する話だけど([これ](https://qiita.com/KenyaSaitoh/items/a04a1e94d28153fd1afb)を読む限り)、
普通に使うと[こういうエラー](https://stackoverflow.com/questions/46501047/what-does-required-filename-based-automodules-detected-warning-mean)が出るし、もうどうすればいいんだ。  

それで、たぶんだけども、このまま使い続けるとコンパイル後にパッケージングするときにエラーが出る……らしい。パッケージのスコープ問題や外部パッケージの読み込み問題とか、問題がわらわらでよくわからない。  
その時になったら考える。

#### 通信関係
全然わからん。シーケンス図がゴミの役にも立たない。そもそもクライアント以外は方向が逆すぎる。どうするのこれ。  
通信待機-通信接続とメッセージの送受信とかクライアント側のことしか考えられてないし、そしてそうしないとシーケンス図が書けないの終わってる。  
ただorderが割り振れたし、企画そのものは整ってるから後はやるしかない……  

***
### 対人関係

#### レビュー
かなりリーダーに負荷がかかっているので、本格的にどうにかしないと不味いと思う。  
でも他にレビューできる人が存在しないし、それぞれタスクが大きすぎる。
自分がレビューすることも考えたけど、今以上のタスクをもって上手くいくとは思えない。自分のタスクが片付いたら助けたい。

#### PRとブランチ
個人的な主義主張を押し付けてしまった気がして、反省しなければならない。  
確かに最適な話はしたと思うけど、もっとわかりやすい方法あったんじゃないかなあ。

#### コミュニケーション
それぞれがそれぞれの対応範囲しか理解してないのは良いんだけども、開発で全く理解していないところをそれぞれ理解しなおす必要があって大変。  
ただまあ、これはリーダーの決定だから素直に従う。  

***
### 他
なんか書く？
