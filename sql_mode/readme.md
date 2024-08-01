現在の状態を確認（GLOBAL）

```sql
SELECT @@GLOBAL.sql_mode;
```


```sql
mysql> SELECT @@GLOBAL.sql_mode;
+-----------------------------------------------------------------------------------------------------------------------+
| @@GLOBAL.sql_mode                                                                                                     |
+-----------------------------------------------------------------------------------------------------------------------+
| ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION |
+-----------------------------------------------------------------------------------------------------------------------+
1 row in set (0.00 sec)
```

今回は「ONLY_FULL_GROUP_BY」を外してみます。<br>
以下のSQLを実行します。


```sql
SET GLOBAL sql_mode = 'STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';
```

<br>

「ONLY_FULL_GROUP_BY」がなくなったことを確認。

```sql
mysql> SELECT @@GLOBAL.sql_mode;
+----------------------------------------------------------------------------------------------------+
| @@GLOBAL.sql_mode                                                                                  |
+----------------------------------------------------------------------------------------------------+
| STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION |
+----------------------------------------------------------------------------------------------------+
1 row in set (0.00 sec)
```
