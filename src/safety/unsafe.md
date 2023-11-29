# Safety

**this program is _unsafe_ or it has _undefined behavior_ (UB)**

```rust,does_not_compile

fn read(y: bool) {
    if y {
        println!("y is true!");
    }
}

fn main() {
    read(x);
    let x = true;
}
```
