# CommandLineTricks
A list of command line tricks for various tasks

## Renaming Files in Bulk

```bash
find /search/path -depth -name '* *' \
 -execdir bash -c 'mv -- "$1" "${1// /_}"' bash {} \;
```
where
```${VARIABLE//PATTERN/REPLACEMENT}``` is the format of the renaming
