# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？


+ リモートリポジトリとは、ネットワーク上に存在するリポジトリ（ファイル、ディレクトリの記録場所）です
+ ローカルリポジトリとは、ネットワークを介さず、各個人のコンピュータの中に存在しているディレクトリです。


## プッシュとマージの違いは何でしょうか？
- プッシュとは、ローカル環境での作業が終了した時にリモートへ作業内容を反映させる作業です。
- マージとは、ブランチで行った作業をマスターへ反映させる作業です。マスターからブランチへのコマンドです。


## コミットとプッシュの違い
- コミットとは、addを行いstagingされた変更内容を保存するコマンドです。
* ローカルの、その作業ブランチ内にしか変更内容が保存されないことがプッシュとの違いだと思います。


## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
* 他の人に対して、自分がどのような変更を行ったのか分かりやすく簡潔に書くことが最適だと思います。


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
- まずローカルでマージするフローでは、作業ブランチでコミットを行い、マスターへ移動します。
- マスターへ移動したらマスターから作業ブランチに対してマージを行い変更内容をローカルのマスターにも反映させます。
- その後プッシュでリモートのマスターにも反映させます。
* 次にプルリクエストでマージするフローでは、作業ブランチでコミットとリモートへのプッシュを行います。
* プッシュ後はリモートでプルリクエストを作成し、他の方のレビューを経てからリモートのマスターへのマー*ジを行います。
* この場合ローカルのマスターには変更内容が反映されていないため、リモートのマスターからプルを要求することでローカルのマスターに変更内容が反映されるようになります。

- 違いとしては、ローカルのマスターに変更内容が反映されるタイミング、他の人の目を受けているかが該当すると思われます。


## コンフリクトを起こしてしまった場合、どう対処すべきですか？
* ソースコードをよく確認し、先の内容を取り込むか、後の内容を取り込むか、両方の内容を取り込むかを判断します。
- 特に３番目ですが、慎重に判断するべきだと思われます。
