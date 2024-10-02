# 使い方
学祭部誌用のpreamble（preamble_p.tex）と本文のtexファイルの雛形（hinagata.tex）を用意しています. 
このリポジトリから2つのファイルを適宜ダウンロードして, cloudlatexのディレクトリに入れて執筆すればすぐに部誌に組み込める書類が出来上がるはずです. 
ちなみにcloudlatexのエンジンは**platex**にしてください. 

状況に合わせてpreambleを適宜更新していく場合があります. 
その場合は更新はここにも反映させます. 

（2024/9/22追記）DeclareMathOperatorコマンドを使いたい人のためにDMO.texというファイルを作成しました. 
これは（更新した）preamble_p.texの中に\input{DMO.tex}という１行があり, このDMO.texに新しく定義する演算子を書くことで使えるようになります. 
**DMOを使わない人でも, これ以降新しくこのpreambleを使ってtexファイルを作成する場合はDMO.texもpreambleと同じディレクトリに入れてください**




# 執筆要綱
1. 「立つ崎」や「はしご高」のような**環境依存文字**を使用する場合は**その旨を明記すること**. 
2. 見出しの深さは原則, 「節」, 「小節」, 「小小節」までです[^1]. 
3. 句読点は, 「, .」統一とします.
4. 引用は, 著者名「書誌名」出版社（もしくはurl）の形式で文章末に明記してください. 
5. 数式番号は文中で引用するもののみ付けてください. 
6. 文字の大きさ, フォント, 用紙の大きさは気にしなくて良いです. 
7. 体裁は基本的に編集側の都合で変更する場合があります. ご了承ください. 
8. 何かあればご相談ください.

[^1]: section, subsection, subsubsectionに対応しています

# TeXで作成してくださる方/TeXにしてくれる方
1. エンジンは**platex**で作成していますので合わせてほしいです. 
2. **環境依存文字**を使用する場合は\UTF{該当するUnicode} で使用してください[^2] .
3. \labelの名前は全てアルファベットで（eqは数式, figは図（写真）, tableは表, secは節を表すものとする）
**\label{titlename:eq/fig/table/sec:jiyunidozo}**
という形式でつけてください.
>[!CAUTION]
>\labelの名前に "_"（アンダーバー）を使うとエラーを吐くので注意
4. 数式を引用する場合は\eqref で引用してください。図表等は\refで構いません. 
5. ファイル名はアルファベットで "titlename.tex" に統一してください.
6. **\qty** は**physicsパッケージ**の使い方に合わせて, **\si等**で**単位や単位つきの量**は記述してください[^3].
7. その他preambleにない機能を使用したい際は気兼ねなく相談してください.
>
>（2024/10/2）文献を引用する際は\cite{}を使用してください




[^2]: 環境依存文字を素で入力してそのtexファイルをplatexでコンパイルするとエラーが起きるはずです. 文字一つのためにエラーを探すのは大変な気がするので気をつけています. 
[^3]: これは編集者の未熟のため\usepackage{physics}と\usepackage{siunitx}をpreambleに記述していて, \qtyコマンドに被りが生まれていることによります. これ原因のエラーが表示されますが, コンパイルに問題はないはずです. 
