# Heap

**a `Box` is used to put data in the heap**

<div class="override-moved">

```aquascope,interpreter,horizontal,run,interpreterControls
fn main() {
    let a = Box::new([0; 1_000_000]); `[]`
    let b = a; `[]`
}
```

</div>
