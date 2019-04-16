# Find and replace on a batch of files
```
find . -name "*.swift" -exec sed -i '' "s/from/to/g" {} + 
```
