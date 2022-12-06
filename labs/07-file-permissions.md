## File permissions

`mkdir /tmp/dir`

`chmod 700 /tmp/dir`

`touch /tmp/dir/file`

`chmod 600 /tmp/dir/file`

---

`chmod u-r /tmp/dir`

`ls -ld /tmp/dir` +

`ls -l /tmp/dir/file` or `stat /tmp/dir/file` +

`cd /tmp/dir` +

`ls -la /tmp/dir` -

`touch /tmp/dir/file2` +

`chmod 700 /tmp/dir`

`cd`

---

`ls -ld /tmp/dir` and `ls -l /tmp/dir/file` or `stat /tmp/dir/file`

`chmod u-x /tmp/dir`

`ls -ld /tmp/dir` +

`ls -l /tmp/dir/file` or `stat /tmp/dir/file` -

`cd /tmp/dir` -

`ls -la /tmp/dir` +-

`touch /tmp/dir/file3` -

`chmod 700 /tmp/dir`

---

`ls -ld /tmp/dir` and `ls -l /tmp/dir/file` or `stat /tmp/dir/file`

`chmod u-w /tmp/dir`

`ls -ld /tmp/dir` +

`cd /tmp/dir` +

`ls -la` +

`> file4` -

`rm file` -

`chmod 700 /tmp/dir`

---

`ls -ld /tmp/dir` and `ls -l /tmp/dir/file` or `stat /tmp/dir/file`

Open new session with 'destroyer' user

`ls -ld /tmp/dir` +

`ls -l /tmp/dir/file` -

`cd /tmp/dir` -

`ls -la /tmp/dir` -

`> /tmp/dir/file5` -

`rm /tmp/dir/file` -

---
5-4

`chmod g+r /tmp/dir/file` (from creator terminal)

From destroyer terminal:

`ls -ld /tmp/dir` +

`ls -l /tmp/dir/file` -

`cd /tmp/dir` -

`ls -la /tmp/dir` -

---
5-5

`chmod g+wx /tmp/dir/file` (from creator terminal)

`ls -ld /tmp/dir` +

`ls -l /tmp/dir/file` +

`cd /tmp/dir` +

`ls -la /tmp/dir` -

---
5-7

`touch /tmp/dir/file7` +

`rm /tmp/dir/file` +

`rm /tmp/dir/*` +

`rmdir /tmp/dir` -

---
6-1

`su root`

`> /append_only`

`man chattr` search 'append'

`chattr +a /append_only`

`echo "text" > /append_only` -

`echo "text" >> /append_only` +

`rm /append_only` -

`chattr -a /append_only`

`rm /append_only` +

---
6-2

`su root`

`> /immutable`

`man chattr` search 'immutable'

`chattr +i /immutable`

`echo "text" > /immutable` -

`echo "text" >> /immutable` -

`rm /immutable` -

`chattr -i /immutable`

`rm /immutable` +


---
[Home](../README.md) -> [Labs](labs.md)
