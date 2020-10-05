# datetime型のカラムをdate型に変換する

## CAST関数を使って変換する

`CAST([datetime型のカラム] AS DATE)`

## 例

以下のようなテーブルを使う

```sql
mysql> SELECT * FROM race_result;
+----+--------+----------------------------+-----------+---------+-----------------+
| id | result | updated_at                 | jockey_id | race_id | thoroughbred_id |
+----+--------+----------------------------+-----------+---------+-----------------+
|  1 |      1 | 2020-08-29 16:00:19.857655 | jockey_1  |       1 | thoroughbred_1  |
|  2 |      2 | 2020-08-29 16:00:19.889192 | jockey_2  |       1 | thoroughbred_2  |
|  3 |      3 | 2020-08-29 16:00:19.891649 | jockey_3  |       1 | thoroughbred_3  |
|  4 |      4 | 2020-08-29 16:00:19.894420 | jockey_4  |       1 | thoroughbred_4  |
|  5 |      5 | 2020-08-29 16:00:19.896605 | jockey_5  |       1 | thoroughbred_5  |
+----+--------+----------------------------+-----------+---------+-----------------+
```

updated_atをdate型としてSELECTする

```sql
mysql> SELECT DISTINCT CAST(updated_at AS DATE) FROM race_result;
+--------------------------+
| CAST(updated_at AS DATE) |
+--------------------------+
| 2020-08-29               |
+--------------------------+
```

`GROUP BY` にも指定できる

```sql
mysql> SELECT count(id), CAST(updated_at AS DATE) FROM race_result GROUP BY CAST(updated_at AS DATE);
+-----------+--------------------------+
| count(id) | CAST(updated_at AS DATE) |
+-----------+--------------------------+
|         5 | 2020-08-29               |
+-----------+--------------------------+
```

## CASTとCONVERT

ちなみに、CONVERT関数でも同様の事が可能

```sql
mysql> SELECT DISTINCT CONVERT(updated_at, DATE) FROM race_result;
+---------------------------+
| CONVERT(updated_at, DATE) |
+---------------------------+
| 2020-08-29                |
+---------------------------+
```

違いとしては、CAST関数は標準SQLの構文だが、`CONVERT(expr,type)`の形式のCONVERT関数はODBCの構文。

ただし、`CONVERT(expr USING transcoding_name)`の形式で文字コードの変換をするのは標準SQLの構文。

CONVERTは文字コードの変換に利用して、CASTは型変換に用いるのが良さそう。

## 参考

- <https://amidagamine.com/notes/3258>
- <https://dev.mysql.com/doc/refman/5.6/ja/cast-functions.html>
