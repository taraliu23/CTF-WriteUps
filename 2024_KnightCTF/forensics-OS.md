## Question

> My boss, Muhammad, sent me this dump file of a memory. He told me that this OS has a malware virus that runs automatically. I need to find some more information about this OS, and the hacker also created some files in this OS. He gave me a task to solve this within 24 hours. I am afraid. Will you please help me? My boss sent some questions; please solve them on my behalf. There are total 7 challenges in this series. Best of luck.
>
> What is the OS version?
>
> Attachment: KnightSquad.DMP
>
> Flag Format: KCTF{1.1.1111.11111}

## Solution

Use [Volatility 3](https://volatility3.readthedocs.io/en/latest/volatility3.html) to check os version

### Step 1: OS type

```shell
strings KnightSquad.DMP > output.txt
```
Use search/ RegEx and find "Windows".

Use search/ RegEx to match version info(wasn't shown)
```shell
grep -E '\\d+\\.\\d+\\.\\d+\\.\\d+' output.txt
```

### Step 2: volatility3
Use windows plugin in volatility3 to check 

```shell
python volatility3-1.0.0/vol.py -f KnightSquad.DMP windows.info
```
![20240120result](https://github.com/drunken-boat/CTF-WriteUps/assets/80751447/ad958a43-6ee0-4965-ac38-7ae8409c3cc5)

### Step 3: flag
~~`KCTF{6.1.7601.24214}`~~

but win7=win6.1

`KCTF{7.1.7601.24214}` (correct!)
