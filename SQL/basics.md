### SQL
→データベースを操作する専用の言語。

### リレーショナルデータベース(RDB)
→複数の表の形式でデータを管理する。
テーブルは行(row、レコード)と列(column、カラム、フィールド)で構成される。

### データベース内のデータの操作の流れ
SQL文をDBMSに送信 → データベース管理システム(DBMS)がSQL文(命令)を受け取る → DBMSがファイル内のテーブルのデータを検索、追加、更新、削除する

### RDBMS
→DBMSのうち、複数の表の形式でデータを取り扱う。
各社からソフトウェア製品として発売されている、オープンソースウェア(OSS)としてインターネト上に無償で公開されているものもある。

### リテラル
→SQL文のなかに書き込まれた具体的なデータそのものの値。

### リテラルの記述のルール
1. [ ’ ]でくくられずに記述されたリテラルは数値情報として扱われる。
2. [ ’ ]でくくられたリテラルは文字列情報として扱われる。
3. [ ’ ]でくくられ、’2024-2-17’ のような一定の形式で記述されたリテラルは日付情報として扱われる。
4. [ ” ]はSQLの文字列リテラルとして用いることはできない。