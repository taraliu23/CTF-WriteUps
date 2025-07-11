* Not original, solution is fully referred from [PIE TIME — picoCTF 2025 by Jin from Medium](https://systemweakness.com/pie-time-picoctf-2025-dbec42ba0857)

```shell
wget https://challenge-files.picoctf.net/c_rescued_float/{instance}/vuln.c

wget https://challenge-files.picoctf.net/c_rescued_float/{instance}/vuln

chmod +x vuln

./vuln

nano vuln.c

gcc vuln.c -o vuln1

./vuln1

gdb ./vuln

(gdb) r 

(gdb) disas main

(gdb) disas win

```

```python
main = input("Enter hex: ")
main = int(main, 16) - 150
main = hex(main)
print(main)
```
