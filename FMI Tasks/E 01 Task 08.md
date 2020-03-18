**Задача 8.** Намерете имената на топ 5 файловете в текущата директория с най-много hardlinks.

*Решение:*

Първи начин:

```sh
stat -f "%l %N" * | sort -rn -t' ' -k1 | head -5 | cut -d' ' -f2- 
```

Втори начин:

```sh
gstat -c "%h %N" * | sort -rn -t' ' -k1 | head -5 | cut -d' ' -f2- 
```