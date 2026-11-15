# Мое домашнее задание № 3

## Задание № 3.1

```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux --sort=-%cpu 1> out.txt 2> /dev/null
```
[Результат](out.txt)

```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux ------- 2> err.txt
```
[Результат с ошибкой](err.txt)

```bash
root@roman-VB:/home/roman/repo/my-third-repo# ps aux | head -11 | tee proc.txt
```
[Топ 10 процессов](proc.txt)

