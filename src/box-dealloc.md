## Boxes are automatically deallocated...

```aquascope,interpreter,horizontal,run,interpreterControls
fn main() {
    let a_num = 4; `[]`
    make_and_drop(); `[]`
}

fn make_and_drop() {
    let a_box = Box::new(5); `[]`
}
```

> **Box deallocation principle (almost correct):** If a variable is bound to a box, when Rust deallocates the variable's frame, then Rust deallocates the box's heap memory.
