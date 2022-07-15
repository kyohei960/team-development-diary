これからチーム開発で気付いたことや得た知識を記述していこうと思います。

1.画像投稿したい際は、２つ方法がある。１つは、カラム名が必要なrefileをgemfileに書いて、画像が必要なテーブルにimage_idとしてidを持たせる
　２つ目は、gemfileをしようせずにActive_Storageをインストールする方法で、
　rails active_storage:install　コマンドを実行する。インストールした
　Active_Storageをrails db:migrateでデータベースに保存して画像が必要なmodelに
　has_one_attached :image を記述する。　後は、画像投稿したいViewに<%= f.file_field :image ~　%>を記述。

2.boolean とは、真と偽のような2つの状態を表すデータ型　booleanを使うときはカラム名をis_deletedなどにしないといけない。

3.列挙型をenumで管理する

4.routes.rbで使われるresourceとresources。resourceはidが生成されず、resourcesはidが生成される。
5.idは会員で例えると他人が第三者の情報などが見れるようにする場合はつける。
6. .gitignoreは不要なファイルや管理の対象外にしたい場合に記述する所
7. 質問したい場所
 ターミナル
【顧客用】
$ rails g devise:views publics

【管理者用】
$ rails g devise:views admins
上記のコマンドで生成された View ファイルは admins フォルダとして作成されるため、admin フォルダに改名を行いましょう。

8.