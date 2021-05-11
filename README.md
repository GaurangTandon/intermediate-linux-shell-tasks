# Mastering intermediate Linux shell usage

I use the shell fairly confidently when dealing with everyday tasks. I have dozens of aliases and helper scripts to get stuff done. But I'm uncomfortable with some Linux commands that are quite uncommon. This is just an attempt to document their practical usages for easy reference/rememberance, and to avoid having to visit purple links on search engines over and over again :D

# `du`

## Best `du` command

Using only `du` gives you recursive unreadable output. `du -h` gets you human-readable file sizes. `du -h --max-depth=1 <dir>` will restrict the recursive output, but not show the files (only directories). Hence, `du -sh <dir>/*` is the best, `-s`ummarize shows both top-level files and folders!

But, do note that the max-depth method shows you the total directory size by default. In the summarize method, you need to separately call `du -sh <dir>` to get total directory size.

## Sort `du -h` output by size

`du -h ... | sort -h`: `sort` takes an argument `-h` which is suitable for handling the human-readable file sizes.

## Filter `du` directories by a size threshold

For example, print directories only with a size of 500MB or more.
TODO:

## Delete last 10 directories 

TODO: 

Grabbing the directory names: `du -h --max-depth=1 <directory> | sort -h | tail -10 | cut -f 2`. Note that `cut` splits input text on columns, and by default, on tab characters (you can specify column delimiter with `-d`).

How to pass them to `rm -r`? need to use `xargs`/`find`?

# `sed`

# `xargs`

Good resource to learn: [TODO]
