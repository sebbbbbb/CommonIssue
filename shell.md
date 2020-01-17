# Find and replace on a batch of files
```shell
find . -name "*.swift" -exec sed -i '' "s/from/to/g" {} + 
```
# Replace extension on a batch of files
```shell
# Ex : rename *.txt to *.html
rename -S .html .txt *.html
```
