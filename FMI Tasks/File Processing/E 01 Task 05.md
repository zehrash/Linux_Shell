**Задача 5.** Напишете серия от команди, извеждащи на екрана само броя на свички обекти във файловата система, чиито собственик е текущия потребител.

*Забележка: Във файловата система със сигурност съществуват директории, до които нямате достъп.*

**Решение:**

```sh
find / -user "$(whoami)" 2>/dev/null | wc -l
```
