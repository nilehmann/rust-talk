## Variables can't be used after being moved

```aquascope,interpreter,horizontal,run,shouldFail
fn main() {
    let first = String::from("Ferris");
    let full = add_suffix(first);
    println!("{full}, original {first}"); `[]`
}

fn add_suffix(mut name: String) -> String {
    name.push_str(" Jr.");
    name
}
```

> **Moved heap data principle:** if a variable x moves ownership of heap data to another variable y, then x cannot be used after the move.
