# Dereferencing a pointer

```aquascope,interpreter
# fn main() {
let mut x: Box<i32> = Box::new(1);
let a: i32 = *x;         // *x reads the heap value, so a = 1 `[]`






#}
```
