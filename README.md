参考文献
http://d.hatena.ne.jp/unageanu/20111031/1320016739
http://d.hatena.ne.jp/nigredo/20091104/1257341341
http://ozzy2010.blogspot.jp/2012/07/seleniumxpath.html

・変更するDcaseのIDは変更すること(deletedcaseのid=d42の42の部分など）

IDEによるテストケース作成時の問題
・指定するボタンがマウスオーバーで出現する場合、それを発見できない
（例：ゴールにマウスオーバー→「出てきた＋ボタン」にマウスオーバー→「出てきたストラテジ」をクリック→テキストボックスに入力）
「」内に記したボタンを、seleniumは発見できない
→mouseoverイベントをfireEventすることで解決
→→トップゴール以外の＋ボタンを押せない問題が発生、解決策を考える
→→→XPathを用いることで解決する

・テキストボックスが閉じない→blurのfireEventを明示的にはさむ
（新規ノード作成のテキストボックスの場合はclick css=#viewer > div）

・store命令を用いて一部の環境変数を前に置いた


selenium rcはテストスイートが必要なため共通のテストケースを1つ使用してスイートを組んでから使う
java -jar selenium-server-standalone-2.33.0.jar  -htmlSuite "*firefox" "http://www.ubicg.ynu.ac.jp/" "/home/kouhei/Developments/seleniumtestcase/seleniumIDE/xxxxx" "/home/kouhei/result"

*firefox
*googlechrome


Seleniumは実行するアプリケーションが別サーバだと実行できない？→別にそんなことない
