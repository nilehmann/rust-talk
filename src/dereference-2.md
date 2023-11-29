# Dereferencing a pointer

```aquascope,interpreter
# fn main() {
let mut x: Box<i32> = Box::new(1);
let a: i32 = *x;         // *x reads the heap value, so a = 1
*x += 1;                 // *x on the left-side modifies the heap value, `[]`






#}
```
