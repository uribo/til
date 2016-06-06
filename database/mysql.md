MySQL
=====

- 接続
    - Amazon RDSへのローカル環境から、踏み台を経由した接続（トンネルを使った接続）
        - ref) http://qiita.com/rjge/items/d9ec5eb463a0ce24cb86
        - 接続が切れたら改めて`ssh`接続を実行

```bash
# エンドポイントの値がhoge.123456789012.us-east-1.rds.amazonaws.com:3306 の場合
ssh -f -N -L 3307:hoge.123456789012.us-east-1.rds.amazonaws.com:3306 -i <hoge.pemへのパス> <踏み台のusername>@<踏み台のhostName>
mysql -u <password> -p -h 127.0.0.1 --port=3307
```

- 既存テーブル内の変数への処理（追加・変更）

```sql
ALTER TABLE [TABLE] CHANGE [COLUMN] old_col_name column_definition;
```
