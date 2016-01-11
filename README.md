# Snapshot of Texas Death Penalty site

This repository is a mirror of the following site:

| Site title  | Death Row Information - Texas Dept. of Criminal Justice |
| URL         | http://www.tdcj.state.tx.us/death_row/                  |
| Mirrored at | 2016-01-11 07:16:39                                     |

You can view the mirrored version by visiting this URL:

http://wgetsnaps.github.io/tdcj-state-tx-us--death_row/death_row/index.html


# How to wget

This is the __wget__ command(s) I used:

~~~sh

# get CSS files
wget --page-requisites \
     --timestamping \
     --convert-links \
     --no-host-directories \
     --adjust-extension \
     --output-file /dev/stdout \
     http://www.tdcj.state.tx.us/death_row/ \
     | tee ./wget.log


# get main site without parents
wget --mirror \
     --timestamping \
     --convert-links \
     --no-host-directories \
     --adjust-extension \
     --no-parent \
     --output-file /dev/stdout \
     http://www.tdcj.state.tx.us/death_row/ \
     | tee ./wget.log
~~~
