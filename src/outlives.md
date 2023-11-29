## A reference can't outlives the data it points to

```aquascope,permissions,stepper,boundaries,shouldFail,run
#fn main() {
let s = String::from("Hello world");
let s_ref = &s;`(focus,rxpaths:s$)`
drop(s);`{}`
println!("{}", s_ref);
#}
```
