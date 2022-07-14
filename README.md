これからチーム開発で気付いたことや得た知識を記述していこうと思います。

1.画像投稿したい際は、２つ方法がある。１つは、カラム名が必要なrefileをgemfileに書いて、画像が必要なテーブルにimage_idとしてidを持たせる
　２つ目は、gemfileをしようせずにActive_Storageをインストールする方法で、
　rails active_storage:install　コマンドを実行する。インストールした
　Active_Storageをrails db:migrateでデータベースに保存して画像が必要なmodelに
　has_one_attached :image を記述する。　後は、画像投稿したいViewに<%= f.file_field :image ~　%>を記述。

2.boolean とは、真と偽のような2つの状態を表すデータ型　booleanを使うときはカラム名をis_deletedなどにしないといけない。

3.列挙型をenumで管理する

4.routes.rbで使われるresourceとresources。resourceはidが生成されず、resourcesはidが生成される。