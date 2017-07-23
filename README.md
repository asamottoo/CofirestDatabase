▪️▪️Cofiest Database▪️▪️

Co(Compact) fi(File) rest(RESTful) Database
読み方

Cofiest Databaseは、ファイル管理を用いてDBの機能を実装するものとなります。
情報へのアクセスはRESTfulなAPIを用いることが特徴となります。

◆Pros
・ライブラリとしての提供であるためサーバーを別途用意する必要はない。
・外部インタフェースの設計がREST APIライクであるためマイクロサービスを扱う感覚で使用できる。
・キャッシュの使用をテーブル毎に設定できるためある程度のチューニングがしやすい。
・戻り値については各種形式にて取得可能(json,yaml,csv等)。
・cliを実装しているためスキーマ定義とrubyのソースコードを同時に作成可能。
・レコードの有効期限を設定することが可能(DBを用意せず過去情報を溜め込む必要がないことを前提とするため)。
・ログ出力に対応。

◆Cons
・トランザクション処理ができない(マイクロサービス向けであるため)。
・権限管理ができない。
・対応している型が少ない(数値型,文字列型,時刻型)。
・メモリ消費量とディスクIOはトレードオフの関係となる。
・リレーションが使用できない。

◆実装項目
・ファイル管理
・スキーマ定義
・情報のread/write
・cliの実装(各種設定変更,テーブルの作成及び変更,レコードの操作)
・キャッシュ機能
・設定ファイル読み込み
・各種戻り値への対応
・cliの実装(ソースコードの自動生成)
・情報の定期削除
・ログの出力
・戻り値の実装(json,yaml,csv)

◆実装検討中
・リレーション
・SQL
・トランザクション
・戻り値の実装(各クラスのインスタンス)
