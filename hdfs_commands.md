**Hadoop HDFS Commands**

Прежде чем приступим, запустим службы Hadoop:

```
sbin/start-dfs.sh
```


_10 лучших команд HDFS_
![10 лучших команд HDFS](https://data-flair.training/blogs/wp-content/uploads/sites/2/2016/06/top-10-hadoop-hdfs-commands.jpg)


1. version
```
hadoop version
```
Команда оболочки Hadoop fs version выводит версию Hadoop.

2. mkdir 
```
hadoop fs -mkdir /newDataFlair
```
Создание директории с именеи newDataFlair

3. ls
```
hadoop fs -ls /
```
Вывод:
`
Found 1 items
drwxr-xr-x   - koffer supergroup          0 2024-01-09 08:18 /newDataFlair
`



