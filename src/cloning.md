# Cloning avoids moves

```aquascope,interpreter,horizontal,run
fn main() {
    let first = String::from("Ferris");
    let first_clone = first.clone(); `[]`
    let full = add_suffix(first_clone); `[]`
    println!("{full}, original {first}");
}

fn add_suffix(mut name: String) -> String {
    name.push_str(" Jr.");
    name
}
```
