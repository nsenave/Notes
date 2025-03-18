# Shell notes

## Difference shell / bash

- https://stackoverflow.com/questions/5725296/difference-between-sh-and-bash
  - https://stackoverflow.com/a/5725402/13425151

## Count lines of code

- https://stackoverflow.com/a/16872227/13425151

Example:

```
# Count lines in '.java' files
find . -type f -name '*.java' | xargs cat | wc -l
# same without counting blank lines
$ find . -type f -name '*.java' | xargs cat | grep -ve '^\s*$' | wc -l
```
