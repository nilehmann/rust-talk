# Drop

```aquascope,interpreter,horizontal,run
fn main() {
    let a = Box::new(42); `[]`
    drop(a); `[]`
}

fn drop(_b: Box<i32>) { }
```
