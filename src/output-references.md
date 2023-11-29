# Flow Permission

```aquascope,permissions,showFlows,boundaries
fn first(strings: &Vec<String>) -> &String {
    let s_ref = &strings[0];
    s_ref`{}`
}
```

- **Flow permission** (@Perm{flow}): expected whenever an expression uses an input reference, or returns an output reference.
- The flow permisison (@Perm{flow}) does not change throughout the body of a function.
