参考文献
http://d.hatena.ne.jp/unageanu/20111031/1320016739

・変更するDcaseのIDは変更すること(deletedcaseのid=d42の42の部分など）

IDEによるテストケース作成時の問題
・指定するボタンがマウスオーバーで出現する場合、それを発見できない
（例：ゴールにマウスオーバー→「出てきた＋ボタン」にマウスオーバー→「出てきたストラテジ」をクリック→テキストボックスに入力）
「」内に記したボタンを、seleniumは発見できない
→mouseoverイベントをfireEventすることで解決
→→トップゴール以外の＋ボタンを押せない問題が発生、解決策を考える

・テキストボックスが閉じない→blurのfireEventを明示的にはさむ
（新規ノード作成のテキストボックスの場合はclick css=#viewer > div）


selenium rcはまだ動かない（以下シェルのコード例）
java -jar selenium-server-standalone-2.33.0.jar  -htmlSuite "*firefox" "http://www.ubicg.ynu.ac.jp/" "/.../signout" "result"

