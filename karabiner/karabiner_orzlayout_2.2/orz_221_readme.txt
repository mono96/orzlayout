Orzレイアウト
~~~~更新履歴~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ver 2.2.1----------------------------------------
20141030
かわせみ2 単語登録 ショートカット option ＋ Ｎ に対応のオプションを詳細モードに準備


Ver 2.2----------------------------------------
20141015

・パスワード入力ダイアログで  orzレイアウトを無効に
・既存の設定を読み込まないようにする
「Use prepared settings」オフの時にエラーが出るのを
解消
・ちょっと個人的に使う設定も追加。

秋も深まってきたのですが、今年も松茸は高値の花でして、
松茸といえば、昔、そういう名前の日本語変換FEP（MS-DOS）
がありました。

ATOKよりもコアなファンの方がたくさんおられたのですが、
気がつけば、、でした。

Macの日本語変換に名前がなくなってしまって、呼びにくいので
名前をつけてもらえませんかね、、。

Ver 2.1----------------------------------------
20140911

Webで配布する間もなく、2.2にアップデートした幻の
パージョンです。親指シフト道場参加の方に配布した。

シンプル設定モードを追加
・日本語入力
・英字入力
・Commandキーショートカット
のorzレイアウト（親指シフトは 左=スペース・右=かな に固定）

「:」キーをDeleteキーに設定するか？のみ選択可能な設定を追加

xml設定ファイルは orzフォルダの中「simpleフォルダ」に格納してあります。
 初めてorzレイアウトを使い始める方が、初期設定を迷わずに設定できる形を
 目指しました。


Ver 2.0----------------------------------------
20141031


### Version 2.0

バージョン表記を改め、Version 2.0として公開します。

### コマンドキー周りを大きく改善

コマンドキーやオブションキーとの組み合わせで、右手のキー配列がずれていなかった組み合わせを修正しました。

どのキーもorzレイアウトで動作するようになりました。Photoshopやイラストレーターなどのショットカットに対応しました。

### ATOKの単語登録ショートカット

従来のバージョンの場合、特定の環境下では、ATOKの単語登録ショートカットが動作しないトラブルがあり、改善しました。

### Sublime Text 2のショートカット

Package Controlを起動するショートカット『cmd+shift+P』を動作するように修正しました。


### 動作がおかしい時は旧バージョンを

定義ファイルを大きく書き換えました。繰り返しテストしておりますが、万が一、アップデートしたことで不安定になった場合は、下の旧バージョンに戻してください。

旧バージョン OrzレイアウトVer.170  → http://www.monochrome-photo.info/?p=17408

よろしくお願いします。


Ver 0.170----------------------------------------
20130927

KeyRemap4MacBook 8.4.0 アップデートにて、発生したorzレイアウト内のバグを修正。

1,orz_combination.xml

下記 <identifier>がトラブル原因 ＿定義ミス＿ のため コメントアウト

<name>カーソルキー PNBF and Control+AE with Orz</name>
            コメントアウト＞＞ <!-- <identifier>remap.orz_cursol_support</identifier> 20130927 del-->
            <include path="orz_cursor.xml" />


2,orz_cursor.xml

2箇所 <identifier>を追記

<name>Control+PNBF to Up/Down/Left/Right</name>
      追記 ＞＞ <identifier>Control_PNBF2Up_Down_Left_Right</identifier>
      <not>{{EMACS_MODE_IGNORE_APPS}}</not>

<name>Control+AE to Command+Left/Right</name>
      追記 ＞＞ <identifier>Control_AE2Command_Left_Righ</identifier>
      <not>{{EMACS_MODE_IGNORE_APPS}}</not>


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Ver 0.162----------------------------------------
201307009

Evernote に対応するため
    Command + shift + i
    Command + shift + o

orz_command.xml 以下のコードを追加


        <name>Command + shift + i	evernote</name>
        <autogen>__KeyToKey__ KeyCode::O ,ModifierFlag::COMMAND_L  , ModifierFlag::SHIFT_L, KeyCode::I ,ModifierFlag::COMMAND_L , ModifierFlag::SHIFT_L </autogen>
        <autogen>__KeyToKey__ KeyCode::O ,ModifierFlag::COMMAND_R  , ModifierFlag::SHIFT_L, KeyCode::I ,ModifierFlag::COMMAND_R , ModifierFlag::SHIFT_L</autogen>
        
                <name>Command + shift + o	evernote</name>
        <autogen>__KeyToKey__ KeyCode::P ,ModifierFlag::COMMAND_L  , ModifierFlag::SHIFT_L, KeyCode::O ,ModifierFlag::COMMAND_L , ModifierFlag::SHIFT_L </autogen>
        <autogen>__KeyToKey__ KeyCode::P ,ModifierFlag::COMMAND_R  , ModifierFlag::SHIFT_L, KeyCode::O ,ModifierFlag::COMMAND_R , ModifierFlag::SHIFT_L</autogen>   



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Ver 0.16----------------------------------------
20130326

orz_base.xml
左右シフトキーの設定を5つ追加

	左シフト＝英数, 右シフト＝スペース
	左シフト＝英数, 右シフト＝かな
	左シフト＝スペース, 右シフト＝右コマンド
	左シフト＝左コマンド, 右シフト＝スペース
	左シフト＝左コマンド, 右シフト＝右コマンド

「EISUU x2 to EISUU」のメニューを表示
orz_kotoeri.xml
	control+ .to「、」の表記ミスを修正


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Ver 0.15----------------------------------------


20130325

orz_command.xml
	
	firefox対応
    	command+6,7,8,9 for book mark of safari 
    
    	command+ 0,+,- for view of safari 
    	ただし  + キー入力のshiftは左のみ対応 
    
    環境設定呼び出し追加
    	Command + ,  で環境設定
    	
------------------------------------------------
    

firefox対応
    command+6,7,8,9 for book mark of safari 
    command+ 0,+,- for view of safari 
    	ただし  + キー入力のshiftは左のみ対応 
    
    環境設定呼び出し追加
    	Command + ,  で環境設定

   
