---
description: Memory forensics framework
---

# Volatility

Основные команды (в порядке последовательности выполнения их)

* imageinfo - определить профиль&#x20;
* pstree - дерево процессов&#x20;
* cmdline - аргументы процессов&#x20;
* procdump - сдампить ехешник&#x20;
* netscan - соединения&#x20;
* filescan - листить файлы&#x20;
* dumpfiles - доставать файлы&#x20;
* bioskbd - клавиатура&#x20;
* clipboard - буфер&#x20;
* consoles - история команд в консоли
* &#x20;hashdump - хеши паролей&#x20;
* iehistory - история IE&#x20;
* screenshot - скриншот&#x20;
* truecryptmaster&#x20;
* truecryptpassphrase&#x20;
* truecryptsummary&#x20;
* printkey - ключи реестра

{% code title="Volatility Example Usage" %}
```bash
volatility -f MyPC-a44c4946.vmem imageinfo
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 pstree
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 procdump --dump-dir .
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 cmdline
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 filescan
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 filescan | grep resume-vm-default.bat
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 dumpfiles -Q 0x000000001df3f1b8 --dump-dir .
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 netscan
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 bioskbd
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 clipboard
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 consoles
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 screenshot --dump-dir .
volatility -f MyPC-a44c4946.vmem --profile=Win7SP1x86_23418 truecryptsummary
```
{% endcode %}

