## Boxes are automatically deallocated..._by the owner_

```aquascope,interpreter,horizontal,run
fn main() {
    let a = Box::new([0; 1_000_000]); `[]` // a owns the box
    let b = a; `[]` // ownership is transfered to b
}
```

> **Box deallocation principle (fully correct):** If a variable _owns_ a box, when Rust deallocates the variable's frame, then Rust deallocates the box's heap memory.
