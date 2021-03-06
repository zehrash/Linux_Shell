**Задача 1.** Напишете серия от команди, които вземат от файла /etc/passwd първите имена на студентите от специалност SI, чиито фамилии завършват на "а". Изведете колко пъти се среща най-често срещаното име и кое е то.

*Примерно съдържание на файла:*

```
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nlogin
s61934:x:1177:504:Mariq Cholakova:/home/SI/s61934:/bin/bash
s61916:x:1178:504:Simeon Aleksandrov:/home/SI/s61934:/bin/bash
s61884:x:1179:504:Ruslan Kapelev:/jome/SI/s61884:/bin/bash
s61895:x:1180:504:Zorka Shindova:/home/SI/s61895:/bin/bash
s61899:x:1182:504:Zorka Ivanova, SI, 2kurs, 5gr:/home/SI/s61899:/bin/bash
s81374:x:1117:503:Ivan Kamburov, KN, 2kurs, 7gr:/home/KN/s81374:/bin/bash
s81382:x:1118:503:Teodora Cirkova:/home/KN/s81382:/bin/bash
```

*Примерен изход:*

```
2 Zorka
```

**Решение:**

Първи начин:

```sh
cat f1 | awk '$0~/\/SI\// {print $0}' |\
awk 'BEGIN{FS="[:,]"}$5~/^[A-Z][a-z]* [A-Z][a-z]*a$/{print $5}' | cut -d' ' -f1 |\
sort | uniq -c | awk '{$1=$1}1' | sort -rn -t' ' -k1 | head -1
```

Втори начин:

```sh
egrep ':[A-Za-z]+ [A-Za-z]*a(:|,).*\/home\/SI' f1 | cut -d ':' -f 5 | cut -d ' ' -f 1 | sort |\
uniq -c | sort -rn | head -n 1
```
