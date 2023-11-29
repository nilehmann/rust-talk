# Safety

**this program is *safe* (to execute)**

```rust
fn read(y: bool) {
    if y {
        println!("y is true!");
    }
}

fn main() {
    let x = true;
    read(x);
}
```

**compiles to assembly**

```x86asm
main:
    ; ...
    mov     edi, 1
    call    read
    ; ...
```
