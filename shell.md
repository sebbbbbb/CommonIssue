# Find and replace on a batch of files
```shell
find . -name "*.swift" -exec sed -i '' "s/from/to/g" {} + 
```
# Replace extension on a batch of files
```shell
# Ex : rename *.txt to *.html
find . -name '*.txt' -exec sh -c 'mv "$0" "${0%.txt}.html"' {} \;
```
