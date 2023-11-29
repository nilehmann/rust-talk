# Lifetimes and control flow

```aquascope,permissions,stepper,boundaries,run
fn ascii_capitalize(v: &mut Vec<char>) {
    let c = &v[0];`(focus,paths:*v)`
    if c.is_ascii_lowercase() {
        let up = c.to_ascii_uppercase();`(focus,paths:*v)`
        v[0] = up;
    } else {`(focus,paths:*v)`
        println!("Already capitalized: {:?}", v);
    }
}
# fn main() {}
```
