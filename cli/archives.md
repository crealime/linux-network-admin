## Archives

`gzip -c some-file > some-file.gz` — add file 'some-file1' to archive 'some-file.gz' (without deleting original)

`gunzip -c some-file.gz` — extract file from archive (archive is saved)

`zcat some-file.gz` — show content of the 'some-file.gz' file

`zmore some-file.gz` `zless some-file.gz`  — page-by-page view contents of the archive

`bzip2 some-file` — compression file with BURROWS-WHEELER algorithm

`bzip2 –d some-file.bz2` — decompression

`bunzip2 some-file.bz2` — decompression

`bzcat some-file.bz2` — show compressed files

`bzip2recover some-file`  — compression/decompression file with BURROWS-WHEELER algorithm

`zcmp some-file.gz` `zdiff some-file1.gz some-file2.gz` — comparison of archives. If the second file is not specified, then the comparison is made with a file without the .gz extension.

`gzexe ./ls` — creating automatically extractable executable files

`gzexe –d ./ls` — decompression

`tar -czf file.tar.gz source.c source.h` — create gzip file archive file.tar.gz from source.c and source.h

`tar -tf file.tar.gz` — read archive content


---

[Home](../README.md) -> [CLI](cli.md)
