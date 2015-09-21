# wbrazilian-without-non-ascii-words

wbrazilian without non-ascii words

Brazilian Portuguese wordlist
This contains part of the wbrazilian wordlist, but with all non-ascii words removed

generated from https://packages.debian.org/en/sid/wbrazilian

```bash
luzfcb@luzfcb:~$ sudo apt-get install wbrazilian
luzfcb@luzfcb:~$ # count words
luzfcb@luzfcb:~$ wc -l /usr/share/dict/brazilian
275502 /usr/share/dict/brazilian
luzfcb@luzfcb:~$ # strip non-ascii words
luzfcb@luzfcb:~$ perl -nle 'print if m{^[[:ascii:]]+$}' /usr/share/dict/brazilian > wbrazilian-without-non-ascii-words.txt
luzfcb@luzfcb:~$ # count words
luzfcb@luzfcb:~$ wc -l wbrazilian-without-non-ascii-words.txt 
204448 wbrazilian-without-non-ascii-words.txt

```


LICENCE: [GNU GENERAL PUBLIC LICENSE v2](LICENCE)
