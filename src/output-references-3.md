# Output references

```aquascope,permissions,shouldFail,run
fn first_or(strings: &Vec<String>, default: &String) -> &String {
    if strings.len() > 0 {
        &strings[0]`{}`
    } else {
        default`{}`
    }
}

fn main() {
    let strings = vec![];
    let default = String::from("default");
    let s = first_or(&strings, &default);
    drop(default);
    println!("{}", s);
}
```
