# Ownership

```aquascope,permissions,run
fn main() {
    println!("Hello world");
}
```

<div class="override-moved">

```aquascope,interpreter,horizontal,run
fn main() {
    let x = Box::new([0; 1_000_000]); `[]`
    let y = x; `[]`
}
```

</div>

```aquascope,permissions,show_flows,boundaries,stepper
fn main() {
    let x = Box::new(0);
    let y = x;

    let n = 0;
    n += 1;
}
```

```aquascope,interpreter,horizontal,run
fn main() {
    let first_name = String::from("Ferris");
    let full_name = add_suffix(first_name);
    println!("{full_name}, originally {first_name}"); // first_name is now used here `[]`
}

fn add_suffix(mut name: String) -> String {
    name.push_str(" Jr.");
    name
}
```

```aquascope,interpreter,horizontal,run
fn main() {
    let x = 1;
    let r = &mut x;
}
```

```rust
fn main() {
    let x = 1;
    let r = &mut x;
}
```
