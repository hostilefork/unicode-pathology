# Checking GitHub's Unicode Normalization

The files in this repository were created in Linux with:

    $ cat /proc/version
    Linux version 5.4.0-42-generic (buildd@lgw01-amd64-038)
    (gcc version 9.3.0 (Ubuntu 9.3.0-10ubuntu2))
    #46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020

    $ echo $'\xc3\xa9.txt' $'e\xcc\x81.txt'
    é.txt é.txt

    $ echo "foo" > $'\xc3\xa9.txt'

    $ echo "bar" > $'e\xcc\x81.txt'

    $ ls
    é.txt  é.txt

The question is how GitHub will treat this situation.
