## Memory can't be freed manually in Rust

**imagine we can free a box manually**

<div class="override-moved">

```aquascope,interpreter,horizontal,run,interpreterControls,shouldFail
fn main() {
    let a = Box::new([0; 1_000_000]); `[]`
    free(a); // like free in C/C++ `[]`
    println!("{}", a[0]); `[]`
}
# fn free<T>(x: T) {}
```

</div>

**(this type of UB is called use after free)**
