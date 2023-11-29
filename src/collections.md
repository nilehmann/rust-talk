## Like boxes, collections<sup>*</sup> own their data

```aquascope,interpreter,horizontal,run,interpreterControls
fn main() {
    let first = String::from("Ferris"); `[]`
    let full = add_suffix(first); `[]`
    println!("{full}");
}

fn add_suffix(mut name: String) -> String {
`[]` name.push_str(" Jr."); `[]`
    name
}
```

**<sup>*</sup>collections like `String`, `Vec` or `HashMap`**
