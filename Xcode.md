```
~/Library/Developer/Xcode/DerivedData # derived data folder
```

## SwiftLint

- pattern templates to fix some 'if/guard let' SwiftLint warnings
  - Replace regular expression for the first part: `(if|guard)(\s+)(let|var) (\w*) = \4([\s,])(?!as)` with: `$1$2$3 $4$5`
  - Or: `(let|var) (\w*) = \2([\s,])(?!as|\?)` with `$1 $2$3`
