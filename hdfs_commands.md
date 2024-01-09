# Hadoop HDFS Commands

Прежде чем приступим, запустим службы Hadoop:

```
sbin/start-dfs.sh
```

_10 лучших команд HDFS_

![10 лучших команд HDFS](https://data-flair.training/blogs/wp-content/uploads/sites/2/2016/06/top-10-hadoop-hdfs-commands.jpg)


1. **version**

```
hadoop version
```
Команда оболочки Hadoop fs version выводит версию Hadoop.

2. **mkdir** 

```
hadoop fs -mkdir /newDataFlair
```
Создание директории с именеи newDataFlair

```
hadoop fs -mkdir -p  /DataFlair/xui
```

3. **ls**

```
hadoop fs -ls /
```
Вывод:

Found 1 items  
drwxr-xr-x   - koffer supergroup          0 2024-01-09 08:18 /newDataFlair  

```
hadoop fs -ls -R /
```

4. **put**

В этом примере мы пытаемся скопировать localfile1 из локальной файловой системы 
в фаловую систему Hadoop.

```
hadoop fs -put localfile1 /newDataFlair
```
Вывод:
-rw-r--r--   1 koffer supergroup         52 2024-01-09 08:40 /newDataFlair/localfile1  

Команда Hadoop fs shell put аналогична команде copyFromLocal, которая копирует файлы 
или директории из локальной файловой системы в целевую файловую систему Hadoop.

5. **copyFromLocal**

```
hadoop fs -copyFromLocal test1 /newDataFlair/copytest
```

6. **get**

Команда get копирует файл или каталог из файловой системы Hadoop локально.
```
hadoop fs -get /newDataFlair .
```

7. **CopyToLocal**

В данном примере мы пытаемся скопировать `copysample`, находящийся в каталоге
`newDataFlair` в HDFS, в локальную файловую систему.
```
hadoop fs -copyToLocal /newDataFlair/copysample .
```

8. **cat**

Просмотрим содержимое файла:
```
koffer@hadoop:~$ hadoop fs -cat /newDataFlair/localfile1
```
Вывод:

asdasda  
123123  
...  

9. **mv**

В этом примере у нас есть каталог `DR1`
```
koffer@hadoop:~$ hadoop fs -ls -R /
drwxr-xr-x   - koffer supergroup          0 2024-01-09 08:58 /DR1
...
```
Перемещаем каталог `DR1` в `/DataFlair`.
```
hadoop fs -mv /DR1 /DataFlair
```

Вывод:

koffer@hadoop:~$ hadoop fs -ls /DataFlair  
Found 2 items  
drwxr-xr-x   - koffer supergroup          0 2024-01-09 08:58 /DataFlair/DR1  
drwxr-xr-x   - koffer supergroup          0 2024-01-09 08:36 /DataFlair/xui  


10. **cp**

В этом примере мы копируем файл `xui`, находящийся в каталоге `/DataFlair` в 
каталог `/newDataFlair`

```
hadoop fs -cp /DataFlair/xui /newDataFlair
```

