# Mutable References

```aquascope,permissions,boundaries,stepper,souldFail,run
#fn main() {
let mut v: Vec<i32> = vec![1, 2, 3];
let num: &mut i32 = &mut v[2]; `{}` `(focus,paths:*num,rxpaths:v)`
*num += 1; `{}`
println!("Third element is {}", *num); `{}` `(focus,paths:*num,rxpaths:v)`
println!("Vector is now {:?}", v); `{}`
#}
```
