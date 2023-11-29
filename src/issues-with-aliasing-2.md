# Issues with aliasing

```aquascope,interpreter,horizontal,shouldFail,run
# fn main() {
let mut v: Vec<i32> = vec![1, 2, 3]; `[]`
let num: &i32 = &v[2]; `[]`
v.push(4); `[]`
println!("Third element is {}", *num); `[]`
#}
```

> **Pointer Safety Principle:** data should never be aliased and mutated at the same time.
