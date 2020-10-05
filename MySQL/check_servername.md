# MySQLから接続しているDBサーバーのホスト名を確認する方法

```:sql
mysql> show variables like 'hostname';
```

下記記事をそのまま参考

<https://qiita.com/nii_yan/items/0265f69370bbdb883655>

MySQLにログインして直接作業する際に、想定通りの環境にログインしているか確認するときとかに使う。
