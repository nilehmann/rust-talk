## Permissions are returned at the end of a reference's lifetime

```aquascope,permissions,boundaries,stepper,souldFail,run
#fn main() {
let mut v: Vec<i32> = vec![1, 2, 3];
let num: &i32 = &v[2]; `{}` `(focus,paths:*num,rxpaths:v)`
println!("Third element is {}", *num); `{}` `(focus,paths:*num,rxpaths:v)`
v.push(4); `{}`
#}
```
