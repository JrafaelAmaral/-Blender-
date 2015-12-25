

# Compact Properties

プロパティシェルフにあるよく使う項目だけをダイアログで表示するアドオン。

プロパティシェルフを極力使いたくない自分用に作ったアドオンです。

リネーム・ワールドの背景・選択オブジェクトをレントゲンに設定など。

アドオンをオンにし、以下を3D View内に手動でショートカット登録してください

     object.compact_prop
















# minimum_space_info.py


Infoヘッダーを極力小さく、有効活用するソースコード。

・スプラッシュスクリーンを一番左に

・シーンとスクリーンを削除

・レンダラの表記を小さく

・選択中のオブジェクトをヘッダーでもリネームできるように

・「Renaming objects addon」を導入していると、INFOヘッダーでも一括リネームできるように



 導入方法
 
これはアドオンではないので、手動で直接Blenderのソースコードを上書きして下さい。
ソースコードを改変するので、自己責任で。
Blenderのバージョンアップ時にはリセットされます。


     1, テキストエディターウィンドウを表示させておく
     2, INFOヘッダーを右クリック >
     3, ソースを編集 >
     4, テキストエディターにソースコードが表示されるので、全選択して、このソースコードの内容を貼り付ける
     5, テキストを保存



# Layer Management_x in properties shelf


 Layer Managementをツールシェルフ(左に出るやつ)からプロパティシェルフ(右に出るやつ)にでるように変更しただけのアドオン。
よく使うレイヤーがツールシェルフにあるのになにかと不便に感じたので、自分はプロパティシェルフに表示させてます。


371行目と521行目を以下のように変更しただけです。
 
    bl_region_type = 'TOOLS' 
    
    ↓    ↓    ↓    ↓
    
    bl_region_type = 'UI'
    

ちょっといじれる人ならどうってことないことですが、そうでない人もいるかと思い投稿しました。
 
 

 
 

===============================================================

===============================================================



# SilentKeyDel.py



現在のフレームのキーを『確認せずに』削除するアドオン。


さいでんかさんのアドオン(saidenka/Blender-Scramble-Addon
https://github.com/saidenka/Blender-Scramble-Addon )にある、『確認せずに削除』系が大変作業が捗るので、キーの削除を自作してみた。
 まともなアドオンが作れたのは初めてなんやで。

※申し訳ないが、ショートカットの登録がまだなので、手動でのデュエル開始を宣言しろ！I☆SO☆NO！！


   単純に、『object.delete_xxx』 を以下の箇所に好きなショートカットで登録しすればいいだけです。

user Preferences >
input >
 3D View > Object Mode
 3D View > Pose  
 Timeline


===============================================================

===============================================================






# Blender-Bookyakuno-config

忘却野のキーコンフィグファイル

† 我以外扱うことの出来ない唯一無二の存在 †


キーコンフィグの参考にするだけでもいいのよ
 
 ===============================================================
 
===============================================================
 
 
  ▼▼このショートカット設定の推奨環境▼▼
  
  
  
  ■  Mac(OS X)推奨
   (Cmdキーを使用しているので)
  
  ■  Ctrlキーをホームポジション小指近くに設定
  (より多くのキーを押しやすくするため)
  
  ■  5ボタンマウス推奨
  (エンターと削除を副ボタンに割り当てる)
  
  
  ■  LMBをセレクトマウスに設定
  (一般的なマウス操作に合わせるため)
  
  ■  外部キーリマップアプリでMMBとRMB入れ替え
  (移動拡縮回転時の座標指定の操作を、押しやすい右クリックでやりたいので。
 それに伴い、RMBが割り当てられている操作を全てMMBに変更した。文中でのRMBは実質MMB。
 私は中ボタンクリックの硬さが死ぬほど嫌いなので、極力使用しない環境にしている。)


  
  
  ■  「Wazou’s Pie Menu」アドオンを使用
  (3Dビューのヘッダーでできることの大半を修飾キー各種 + MMBに割り当て)
  Scripts-Blender/Wazou_Pie_Menus at master · pitiwazou/Scripts-Blender
  https://github.com/pitiwazou/Scripts-Blender/blob/master/Wazou_Pie_Menus
  
  
  
  ■  テンキー、「テンキーを模倣」を使用しない
  視点変更は、123/Ctrl + 123に割り当てて場所を節約
  数値入力は、karabinerを使用してQキーを押している間キーボード左側が一時的にテンキーになるように設定
  
  
  
  
  
  
  ===============================================================
  ===============================================================



↓ ショートカット変更点 ↓


  

◆視点変更
123/Ctrl + 123
場所を節約、かつ視点変更のショートカットを整理するため

◆カメラ
4
現在の視点にカメラを合わせる
4 + Ctrl
フライナビゲーション
4 + Ctrl + alt


◆画像レンダリング
5


◆サブディビジョンレベル
Cmd + 1 ……サブディビジョンレベル0
Cmd + 3 ……サブディビジョンレベル2

◆AutoMiller(編集モード中にもミラーを適応できるアドオン)
Cmd + 4

◆ミラー
Cmd + Ctrl + 4


◆適用(回転と拡縮)
Shift + Cmd + 6
ミラーやラジアルクローンなどがうまくいかない時に





◆LMBドラッグを矩形選択に
一般的なマウス操作に合わせるため。選択方法としてもやりやすいため。

◆選択部分を表示

◆全てを表示



◆マウスでの視点操作
Cmd + LMB ……視点を回転
Cmd + RMB ……視点を移動

◆煩わしいメッシュ削除
さいでんか氏のアドオンセットScramble Addonにある、「メッシュ選択モードと同じ要素を削除する」で解消
溶解は、「選択に溶解」を alt + delete に設定


◆パイメニュー アドオンをRMB + 修飾キーにまとめる
RMB + Shift + alt ……シェーディング
RMB + Ctrl + alt ……座標系
RMB + Cmd + alt ……スナップ対象
RMB + Shift + Ctrl ……編集モード時のツールシェルフでできること各種
RMB + Shift ……プリミティブ追加



◆スナップ / プロポーショナル編集 のオンオフ
V / B
Mayaライクに



◆
7 ……選択物にカーソルを設定
7ダブルクリック……カーソル
8 ……カーソル位置に原点に設定
※自分はこれを20ボタンマウスに設定しているが、
 そうでない場合は5ボタンマウスで 
 alt + エンターなどのように割り当てるといいかもしれない。




◆ナイフ
Ctrl + Z







◆移動 / 拡縮 / 回転
A/S/D
左手で押しやすく、XYZキーの近くするため


◆外部キーリマップアプリで、CキーをYキーに入れ替え
XYZのキーを揃えるため
※文字打ちの時にCキーが押せなくなるので、CのタイプはCtrl + Cに割り当て



◆対話モード変更をTab + 修飾キーにまとめる
Tab ……編集
Tabダブルクリック ……オブジェクト
Tab + Shift ……スカルプト
Tab + Ctrl  ……ポーズ
Tab + Ctrl  ……ウェイトペイント
Tab + alt  ……テクスチャペイント




▼スカルプト
アルファベット各種に設定

Q/W/E ……ブラシ / Flatten(平らにする) / Clay Strips(ちょっとずつ塗りつける？)
A/S/D ……ブラシサイズ変更 / スムース / Grab(つまむ)


◆Blender終了をCmd + Qダブルクリックに
(著者はkarabinerでアプリ全てに適応)





◆ウィンドウ切り替え
Shift + F1,F2,F2ダブルクリック,F3,F4,F5
3Dビュー、アウトライナー、プロパティ、ユーザー設定、UV/画像エディター、ノードエディター
(実際はパイメニューを使って済ませることが多い)


◆スプラッシュスクリーン
Cmd + 0
最近使った項目に素早くアクセスするため。
ちなみにダブルクリックで最近開いたファイルで最新のものを開く。



その他諸々





