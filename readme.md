## Yarn does not dedupe nested dependencies

So, I have a repo with four dependencies:

```
diokuz-yarn-nested-dedupe-a
diokuz-yarn-nested-dedupe-b
diokuz-yarn-nested-dedupe-c
diokuz-yarn-nested-dedupe-d
```

`a` and `b` depends on `diokuz-yarn-nested-dedupe-dep@1.0.0`, but `c` and `d` depends on `diokuz-yarn-nested-dedupe-dep@2.0.0`

1.0.0 is deduped to root `node_modules`, but there are two absolutely equal versions of 2.0.0 version in `diokuz-yarn-nested-dedupe-c/node_modules` and in `diokuz-yarn-nested-dedupe-d/node_modules`.

WHY?
